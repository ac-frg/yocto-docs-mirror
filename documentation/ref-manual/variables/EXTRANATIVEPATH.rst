A list of subdirectories of
``${``\ :term:`STAGING_BINDIR_NATIVE`\ ``}``
added to the beginning of the environment variable ``PATH``. As an
example, the following prepends
"${STAGING_BINDIR_NATIVE}/foo:${STAGING_BINDIR_NATIVE}/bar:" to
``PATH``::

   EXTRANATIVEPATH = "foo bar"
