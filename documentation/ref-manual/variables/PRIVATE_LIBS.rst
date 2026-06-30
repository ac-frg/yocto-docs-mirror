Specifies libraries installed within a recipe that should be ignored
by the OpenEmbedded build system's shared library resolver. This
variable is typically used when software being built by a recipe has
its own private versions of a library normally provided by another
recipe. In this case, you would not want the package containing the
private libraries to be set as a dependency on other unrelated
packages that should instead depend on the package providing the
standard version of the library.

Libraries specified in this variable should be specified by their
file name. For example, from the Firefox recipe in meta-browser::

   PRIVATE_LIBS = "libmozjs.so \
                   libxpcom.so \
                   libnspr4.so \
                   libxul.so \
                   libmozalloc.so \
                   libplc4.so \
                   libplds4.so"

For more information, see the
":ref:`overview-manual/concepts:automatically added runtime dependencies`"
section in the Yocto Project Overview and Concepts Manual.
