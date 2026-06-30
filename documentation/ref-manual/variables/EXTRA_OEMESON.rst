Additional `Meson <https://mesonbuild.com/>`__ options. See the
:ref:`ref-classes-meson` class for additional information.

In addition to standard Meson options, such options correspond to
`Meson build options <https://mesonbuild.com/Build-options.html>`__
defined in the ``meson_options.txt`` file in the sources to build.
Here is an example::

   EXTRA_OEMESON = "-Dpython=disabled -Dvalgrind=disabled"

Note that any custom value for the Meson ``--buildtype`` option
should be set through the :term:`MESON_BUILDTYPE` variable.
