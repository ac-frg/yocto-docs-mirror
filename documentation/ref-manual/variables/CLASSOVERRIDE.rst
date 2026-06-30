An internal variable specifying the special class override that
should currently apply (e.g. "class-target", "class-native", and so
forth). The classes that use this variable (e.g.
:ref:`ref-classes-native`, :ref:`ref-classes-nativesdk`, and so forth)
set the variable to appropriate values.

.. note::

   :term:`CLASSOVERRIDE` gets its default "class-target" value from the
   ``bitbake.conf`` file.

As an example, the following override allows you to install extra
files, but only when building for the target::

   do_install:append:class-target() {
       install my-extra-file ${D}${sysconfdir}
   }

Here is an example where ``FOO`` is set to
"native" when building for the build host, and to "other" when not
building for the build host::

   FOO:class-native = "native"
   FOO = "other"

The underlying mechanism behind :term:`CLASSOVERRIDE` is simply
that it is included in the default value of
:term:`OVERRIDES`.
