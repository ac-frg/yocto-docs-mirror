This is similar to :term:`RECIPE_SYSROOT` but files in it are provided by
native recipes. This allows a recipe built for the target machine to
use native tools.

This variable is used to define :term:`STAGING_DIR_NATIVE`.

The default value is ``"${WORKDIR}/recipe-sysroot-native"``.
Do not modify it.
