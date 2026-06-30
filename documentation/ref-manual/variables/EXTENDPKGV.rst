The full package version specification as it appears on the final
packages produced by a recipe. The variable's value is normally used
to fix a runtime dependency to the exact same version of another
package in the same recipe::

   RDEPENDS:${PN}-additional-module = "${PN} (= ${EXTENDPKGV})"

The dependency relationships are intended to force the package
manager to upgrade these types of packages in lock-step.
