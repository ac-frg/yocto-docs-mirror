Converts the newly unpacked kernel source into a form with which the
OpenEmbedded build system can work. Because the kernel source can be
fetched in several different ways, the :term:`do_kernel_checkout` task makes
sure that subsequent tasks are given a clean working tree copy of the
kernel with the correct branches checked out.
