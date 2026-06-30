Prevents specific packages from being installed when you are
installing complementary packages.

You might find that you want to prevent installing certain packages
when you are installing complementary packages. For example, if you
are using :term:`IMAGE_FEATURES` to install
``dev-pkgs``, you might not want to install all packages from a
particular multilib. If you find yourself in this situation, you can
use the :term:`PACKAGE_EXCLUDE_COMPLEMENTARY` variable to specify regular
expressions to match the packages you want to exclude.
