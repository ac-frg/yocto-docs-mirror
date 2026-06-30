This variable holds extra options passed to the compiler and the linker
for non ``-native`` recipes as they have to point to their custom
``sysroot`` folder pointed to by :term:`RECIPE_SYSROOT`::

   TOOLCHAIN_OPTIONS = " --sysroot=${RECIPE_SYSROOT}"

Native recipes don't need this variable to be set, as they are
built for the host machine with the native compiler.
