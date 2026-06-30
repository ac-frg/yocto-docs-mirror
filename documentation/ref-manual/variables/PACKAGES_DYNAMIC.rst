A promise that your recipe satisfies runtime dependencies for
optional modules that are found in other recipes.
:term:`PACKAGES_DYNAMIC` does not actually satisfy the dependencies, it
only states that they should be satisfied. For example, if a hard,
runtime dependency (:term:`RDEPENDS`) of another
package is satisfied at build time through the :term:`PACKAGES_DYNAMIC`
variable, but a package with the module name is never actually
produced, then the other package will be broken. Thus, if you attempt
to include that package in an image, you will get a dependency
failure from the packaging system during the
:term:`do_rootfs` task.

Typically, if there is a chance that such a situation can occur and
the package that is not created is valid without the dependency being
satisfied, then you should use :term:`RRECOMMENDS`
(a soft runtime dependency) instead of :term:`RDEPENDS`.

For an example of how to use the :term:`PACKAGES_DYNAMIC` variable when
you are splitting packages, see the
":ref:`dev-manual/packages:handling optional module packaging`"
section in the Yocto Project Development Tasks Manual.
