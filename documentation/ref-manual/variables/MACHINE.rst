Specifies the target device for which the image is built. You define
:term:`MACHINE` in the ``local.conf`` file found in the
:term:`Build Directory`. By default, :term:`MACHINE` is set to
"qemux86", which is an x86-based architecture machine to be emulated
using QEMU::

   MACHINE ?= "qemux86"

The variable corresponds to a machine configuration file of the same
name, through which machine-specific configurations are set. Thus,
when :term:`MACHINE` is set to "qemux86", the corresponding
``qemux86.conf`` machine configuration file can be found in
:term:`OpenEmbedded-Core (OE-Core)` in
``meta/conf/machine``.

The list of machines supported by the Yocto Project as shipped
include the following::

   MACHINE ?= "qemuarm"
   MACHINE ?= "qemuarm64"
   MACHINE ?= "qemumips"
   MACHINE ?= "qemumips64"
   MACHINE ?= "qemuppc"
   MACHINE ?= "qemux86"
   MACHINE ?= "qemux86-64"
   MACHINE ?= "genericx86"
   MACHINE ?= "genericx86-64"
   MACHINE ?= "beaglebone"

The last five are Yocto Project reference hardware
boards, which are provided in the ``meta-yocto-bsp`` layer.

.. note::

   Adding additional Board Support Package (BSP) layers to your
   configuration adds new possible settings for :term:`MACHINE`.
