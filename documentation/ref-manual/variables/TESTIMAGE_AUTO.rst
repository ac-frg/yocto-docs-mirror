Automatically runs the series of automated tests for images when an
image is successfully built. Setting :term:`TESTIMAGE_AUTO` to "1" causes
any image that successfully builds to automatically boot under QEMU.
Using the variable also adds in dependencies so that any SDK for
which testing is requested is automatically built first.

These tests are written in Python making use of the ``unittest``
module, and the majority of them run commands on the target system
over ``ssh``. You can set this variable to "1" in your ``local.conf``
file in the :term:`Build Directory` to have the
OpenEmbedded build system automatically run these tests after an
image successfully builds:

   TESTIMAGE_AUTO = "1"

For more information
on enabling, running, and writing these tests, see the
":ref:`test-manual/runtime-testing:performing automated runtime testing`"
section in the Yocto Project Test Environment Manual and the
":ref:`ref-classes-testimage`" section.
