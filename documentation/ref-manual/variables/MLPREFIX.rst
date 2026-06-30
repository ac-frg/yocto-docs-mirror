Specifies a prefix has been added to :term:`PN` to create a
special version of a recipe or package (i.e. a Multilib version). The
variable is used in places where the prefix needs to be added to or
removed from a name (e.g. the :term:`BPN` variable).
:term:`MLPREFIX` gets set when a prefix has been added to :term:`PN`.

.. note::

   The "ML" in :term:`MLPREFIX` stands for "MultiLib". This representation
   is historical and comes from a time when ":ref:`ref-classes-nativesdk`"
   was a suffix rather than a prefix on the recipe name. When
   ":ref:`ref-classes-nativesdk`" was turned into a prefix, it made sense
   to set :term:`MLPREFIX` for it as well.

To help understand when :term:`MLPREFIX` might be needed, consider when
:term:`BBCLASSEXTEND` is used to provide a :ref:`ref-classes-nativesdk`
version of a recipe in addition to the target version. If that recipe
declares build-time dependencies on tasks in other recipes by using
:term:`DEPENDS`, then a dependency on "foo" will automatically get
rewritten to a dependency on "nativesdk-foo". However, dependencies like
the following will not get rewritten automatically::

   do_foo[depends] += "recipe:do_foo"

If you want such a dependency to also get transformed, you can do the
following::

   do_foo[depends] += "${MLPREFIX}recipe:do_foo"
