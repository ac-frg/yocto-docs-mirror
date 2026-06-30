When using the Go "vendor" mechanism to bring in dependencies for a Go
package, the default :term:`GO_INSTALL` setting, which uses the ``...``
wildcard, will include the vendored packages in the build, which produces
incorrect results.

There are also some Go packages that are structured poorly, so that the
``...`` wildcard results in building example or test code that should not
be included in the build, or could fail to build.

This optional variable allows for filtering out a subset of the sources.
It defaults to excluding everything under the ``vendor`` subdirectory
under package's main directory. This is the normal location for vendored
packages, but it can be overridden by a recipe to filter out other
subdirectories if needed.
