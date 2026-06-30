The short (72 characters or less) summary of the binary package for
packaging systems such as ``opkg``, ``rpm``, or ``dpkg``. By default,
:term:`SUMMARY` is used to define the
:term:`DESCRIPTION` variable if :term:`DESCRIPTION` is
not set in the recipe.

If you don't set this variable in your recipe file, you will be warned
about that and it will be set to a default value from the
:oecore_path:`meta/conf/bitbake.conf` file.
