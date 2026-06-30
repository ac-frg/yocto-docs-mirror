This variable, which is set in the ``local.conf`` configuration file
found in the ``conf`` folder of the
:term:`Build Directory`, specifies the package manager the
OpenEmbedded build system uses when packaging data.

You can provide one or more of the following arguments for the
variable::

   PACKAGE_CLASSES ?= "package_rpm package_deb package_ipk"

The build system uses only the first argument in the list as the
package manager when creating your image or SDK. However, packages
will be created using any additional packaging classes you specify.
For example, if you use the following in your ``local.conf`` file::

   PACKAGE_CLASSES ?= "package_ipk"

The OpenEmbedded build system uses
the IPK package manager to create your image or SDK.

For information on packaging and build performance effects as a
result of the package manager in use, see the
":ref:`ref-classes-package`" section.
