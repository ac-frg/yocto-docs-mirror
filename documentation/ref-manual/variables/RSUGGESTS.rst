A list of additional packages that you can suggest for installation
by the package manager at the time a package is installed. Not all
package managers support this functionality. This feature takes effect
only when the package manager is being used to install packages on
the target system from a package feed.

As with all package-controlling variables, you must always use this
variable in conjunction with a package name override. Here is an
example::

   RSUGGESTS:${PN} = "useful_package another_package"

For more information on package management, see the
:ref:`dev-manual/packages:Using Runtime Package Management` section
of the Yocto Project Development Tasks Manual.
