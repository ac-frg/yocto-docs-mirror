When inheriting the :ref:`ref-classes-uninative` class, the
:term:`UNINATIVE_CHECKSUM` variable flags contain the checksums of the
uninative tarball as specified by the :term:`UNINATIVE_URL` variable.
There should be one checksum per tarballs published at
:term:`UNINATIVE_URL`, which match architectures. For example::

   UNINATIVE_CHECKSUM[aarch64] ?= "812045d826b7fda88944055e8526b95a5a9440bfef608d5b53fd52faab49bf85"
   UNINATIVE_CHECKSUM[i686] ?= "5cc28efd0c15a75de4bcb147c6cce65f1c1c9d442173a220f08427f40a3ffa09"
   UNINATIVE_CHECKSUM[x86_64] ?= "4c03d1ed2b7b4e823aca4a1a23d8f2e322f1770fc10e859adcede5777aff4f3a"
