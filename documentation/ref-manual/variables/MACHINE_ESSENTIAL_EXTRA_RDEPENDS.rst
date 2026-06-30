A list of required machine-specific packages to install as part of
the image being built. The build process depends on these packages
being present. Furthermore, because this is a "machine-essential"
variable, the list of packages are essential for the machine to boot.
The impact of this variable affects images based on
``packagegroup-core-boot``, including the ``core-image-minimal``
image.

This variable is similar to the
:term:`MACHINE_ESSENTIAL_EXTRA_RRECOMMENDS` variable with the exception
that the image being built has a build dependency on the variable's
list of packages. In other words, the image will not build if a file
in this list is not found.

As an example, suppose the machine for which you are building
requires ``example-init`` to be run during boot to initialize the
hardware. In this case, you would use the following in the machine's
``.conf`` configuration file::

   MACHINE_ESSENTIAL_EXTRA_RDEPENDS += "example-init"
