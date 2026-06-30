This variable provides a means of enabling or disabling features of a
recipe on a per-recipe basis. :term:`PACKAGECONFIG` blocks are defined in
recipes when you specify features and then arguments that define
feature behaviors. Here is the basic block structure (broken over
multiple lines for readability)::

   PACKAGECONFIG ??= "f1 f2 f3 ..."
   PACKAGECONFIG[f1] = "\
       --with-f1, \
       --without-f1, \
       build-deps-for-f1, \
       runtime-deps-for-f1, \
       runtime-recommends-for-f1, \
       packageconfig-conflicts-for-f1"
   PACKAGECONFIG[f2] = "\
        ... and so on and so on ...

The :term:`PACKAGECONFIG` variable itself specifies a space-separated
list of the features to enable. Following the features, you can
determine the behavior of each feature by providing up to six
order-dependent arguments, which are separated by commas. You can
omit any argument you like but must retain the separating commas. The
order is important and specifies the following:

#. Extra arguments that should be added to :term:`PACKAGECONFIG_CONFARGS`
   if the feature is enabled.

#. Extra arguments that should be added to :term:`PACKAGECONFIG_CONFARGS`
   if the feature is disabled.

#. Additional build dependencies (:term:`DEPENDS`)
   that should be added if the feature is enabled.

#. Additional runtime dependencies (:term:`RDEPENDS`)
   that should be added if the feature is enabled.

#. Additional runtime recommendations
   (:term:`RRECOMMENDS`) that should be added if
   the feature is enabled.

#. Any conflicting (that is, mutually exclusive) :term:`PACKAGECONFIG`
   settings for this feature.

Consider the following :term:`PACKAGECONFIG` block taken from the
``librsvg`` recipe. In this example the feature is ``gtk``, which has
three arguments that determine the feature's behavior::

   PACKAGECONFIG[gtk] = "--with-gtk3,--without-gtk3,gtk+3"

The
``--with-gtk3`` and ``gtk+3`` arguments apply only if the feature is
enabled. In this case, ``--with-gtk3`` is added to the configure
script argument list and ``gtk+3`` is added to :term:`DEPENDS`. On the
other hand, if the feature is disabled say through a ``.bbappend``
file in another layer, then the second argument ``--without-gtk3`` is
added to the configure script instead.

The basic :term:`PACKAGECONFIG` structure previously described holds true
regardless of whether you are creating a block or changing a block.
When creating a block, use the structure inside your recipe.

If you want to change an existing :term:`PACKAGECONFIG` block, you can do
so one of two ways:

-  *Append file:* Create an append file named
   ``recipename.bbappend`` in your layer and override the value of
   :term:`PACKAGECONFIG`. You can either completely override the
   variable::

      PACKAGECONFIG = "f4 f5"

   Or, you can just append the variable::

      PACKAGECONFIG:append = " f4"

-  *Configuration file:* This method is identical to changing the
   block through an append file except you edit your ``local.conf``
   or ``mydistro.conf`` file. As with append files previously
   described, you can either completely override the variable::

      PACKAGECONFIG:pn-recipename = "f4 f5"

   Or, you can just amend the variable::

      PACKAGECONFIG:append:pn-recipename = " f4"

Consider the following example of a :ref:`ref-classes-cmake` recipe with a systemd service
in which :term:`PACKAGECONFIG` is used to transform the systemd service
into a feature that can be easily enabled or disabled via :term:`PACKAGECONFIG`::

   example.c
   example.service
   CMakeLists.txt

The ``CMakeLists.txt`` file contains::

   if(WITH_SYSTEMD)
      install(FILES ${PROJECT_SOURCE_DIR}/example.service DESTINATION /etc/systemd/systemd)
   endif(WITH_SYSTEMD)

In order to enable the installation of ``example.service`` we need to
ensure that ``-DWITH_SYSTEMD=ON`` is passed to the ``cmake`` command
execution.  Recipes that have ``CMakeLists.txt`` generally inherit the
:ref:`ref-classes-cmake` class, that runs ``cmake`` with
:term:`EXTRA_OECMAKE`, which :term:`PACKAGECONFIG_CONFARGS` will be
appended to.  Now, knowing that :term:`PACKAGECONFIG_CONFARGS` is
automatically filled with either the first or second element of
:term:`PACKAGECONFIG` flag value, the recipe would be like::

   inherit cmake
   PACKAGECONFIG = "systemd"
   PACKAGECONFIG[systemd] = "-DWITH_SYSTEMD=ON,-DWITH_SYSTEMD=OFF"

A side note to this recipe is to check if ``systemd`` is in fact the used :term:`INIT_MANAGER`
or not::

   PACKAGECONFIG = "${@'systemd' if d.getVar('INIT_MANAGER') == 'systemd' else ''}"
