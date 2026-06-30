When kernel configuration fragments are missing for some
:term:`KERNEL_FEATURES` specified by layers or BSPs,
building and configuring the kernel stops with an error.

You can turn these errors into warnings by setting the
following in ``conf/local.conf``::

   KERNEL_DANGLING_FEATURES_WARN_ONLY = "1"

You will still be warned that runtime issues may occur,
but at least the kernel configuration and build process will
be allowed to continue.
