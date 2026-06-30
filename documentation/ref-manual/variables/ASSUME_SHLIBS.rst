Provides additional ``shlibs`` provider mapping information, which
adds to or overwrites the information provided automatically by the
system. Separate multiple entries using spaces.

As an example, use the following form to add an ``shlib`` provider of
shlibname in packagename with the optional version::

   shlibname:packagename[_version]

Here is an example that adds a shared library named ``libEGL.so.1``
as being provided by the ``libegl-implementation`` package::

   ASSUME_SHLIBS = "libEGL.so.1:libegl-implementation"
