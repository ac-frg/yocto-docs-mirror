Allows to set C compiler options, such as ``-fdebug-prefix-map``,
``-fmacro-prefix-map``, and ``-ffile-prefix-map``, which allow to
replace build-time paths by install-time ones in the debugging sections
of binaries.  This makes compiler output files location independent,
at the cost of having to pass an extra command to tell the debugger
where source files are.

This is used by the Yocto Project to guarantee
:doc:`/test-manual/reproducible-builds` even when the source code of
a package uses the ``__FILE__`` or ``assert()`` macros. See the
`reproducible-builds.org <https://reproducible-builds.org/docs/build-path/>`__
website for details.

This variable is set in the ``meta/conf/bitbake.conf`` file. It is
not intended to be user-configurable.
