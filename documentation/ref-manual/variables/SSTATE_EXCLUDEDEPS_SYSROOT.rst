This variable allows to specify indirect dependencies to exclude
from sysroots, for example to avoid the situations when a dependency on
any ``-native`` recipe will pull in all dependencies of that recipe
in the recipe sysroot. This behaviour might not always be wanted,
for example when that ``-native`` recipe depends on build tools
that are not relevant for the current recipe.

This way, irrelevant dependencies are ignored, which could have
prevented the reuse of prebuilt artifacts stored in the Shared
State Cache.

:term:`SSTATE_EXCLUDEDEPS_SYSROOT` is evaluated as two regular
expressions of recipe and dependency to ignore. An example
is the rule in :oe_git:`meta/conf/layer.conf </openembedded-core/tree/meta/conf/layer.conf>`::

   # Nothing needs to depend on libc-initial
   # base-passwd/shadow-sysroot don't need their dependencies
   SSTATE_EXCLUDEDEPS_SYSROOT += "\
       .*->.*-initial.* \
       .*(base-passwd|shadow-sysroot)->.* \
   "

The ``->`` substring represents the dependency between
the two regular expressions.
