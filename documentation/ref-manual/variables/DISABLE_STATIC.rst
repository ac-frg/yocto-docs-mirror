Used in order to disable static linking by default (in order to save
space, since static libraries are often unused in embedded systems.)
The default value is " --disable-static", however it can be set to ""
in order to enable static linking if desired. Certain recipes do this
individually, and also there is a
``meta/conf/distro/include/no-static-libs.inc`` include file that
disables static linking for a number of recipes. Some software
packages or build tools (such as CMake) have explicit support for
enabling / disabling static linking, and in those cases
:term:`DISABLE_STATIC` is not used.
