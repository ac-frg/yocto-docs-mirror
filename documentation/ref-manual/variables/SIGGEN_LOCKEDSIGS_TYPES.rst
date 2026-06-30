Allowed overrides for :term:`SIGGEN_LOCKEDSIGS`. This is mainly used
for architecture specific locks. A common value for
:term:`SIGGEN_LOCKEDSIGS_TYPES` is ``${PACKAGE_ARCHS}``::

  SIGGEN_LOCKEDSIGS_TYPES += "${PACKAGE_ARCHS}"

  SIGGEN_LOCKEDSIGS_core2-64 += "bc:do_compile:09772aa4532512baf96d433484f27234d4b7c11dd9cda0d6f56fa1b7ce6f25f0"
  SIGGEN_LOCKEDSIGS_cortexa57 += "bc:do_compile:12178eb6d55ef602a8fe638e49862fd247e07b228f0f08967697b655bfe4bb61"

Here, the ``do_compile`` task from ``bc`` will be locked only for
``core2-64`` and ``cortexa57`` but not for other architectures such as
``mips32r2``.
