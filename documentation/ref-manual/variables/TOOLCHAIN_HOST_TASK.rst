This variable lists packages the OpenEmbedded build system uses when
building an SDK, which contains a cross-development environment. The
packages specified by this variable are part of the toolchain set
that runs on the :term:`SDKMACHINE`, and each
package should usually have the prefix ``nativesdk-``. For example,
consider the following command when building an SDK::

   $ bitbake -c populate_sdk imagename

In this case, a default list of packages is
set in this variable, but you can add additional packages to the
list. See the
":ref:`sdk-manual/appendix-customizing-standard:adding individual packages to the standard sdk`" section
in the Yocto Project Application Development and the Extensible
Software Development Kit (eSDK) manual for more information.

For background information on cross-development toolchains in the
Yocto Project development environment, see the
":ref:`sdk-manual/intro:the cross-development toolchain`"
section in the Yocto Project Overview and Concepts Manual. For
information on setting up a cross-development environment, see the
:doc:`/sdk-manual/index` manual.

Note that this variable applies to building an SDK, not an eSDK,
in which case the :term:`TOOLCHAIN_HOST_TASK_ESDK` setting should be
used instead.
