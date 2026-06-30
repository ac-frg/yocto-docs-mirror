Set build target(s) for build reproducibility testing but activate
:ref:`shared state <overview-manual/concepts:shared state cache>` build
for most dependencies (i.e. the ones explicitly listed in DEPENDS, which
may not be all dependencies, c.f. [depends] varflags, PACKAGE_DEPENDS and
other implementations). See :doc:`/test-manual/reproducible-builds`.
