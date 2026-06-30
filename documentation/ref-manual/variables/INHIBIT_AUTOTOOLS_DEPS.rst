Prevents the :ref:`ref-classes-autotools` class from automatically adding
its default build-time dependencies.

When a recipe inherits the :ref:`ref-classes-autotools` class, several
native cross tools such as ``autoconf-native``, ``automake-native``,
``libtool-native``, ``libtool-cross`` are added to :term:`DEPENDS` to
support the ``autotools`` build process.

To prevent the build system from adding these dependencies automatically,
set the :term:`INHIBIT_AUTOTOOLS_DEPS` variable as follows::

   INHIBIT_AUTOTOOLS_DEPS = "1"

By default, the value of :term:`INHIBIT_AUTOTOOLS_DEPS` is empty. Setting
it to "0" does not disable inhibition. Only the empty string will disable
inhibition.
