Points to the directory containing the kernel build artifacts.
Recipes building software that needs to access kernel build artifacts
(e.g. ``systemtap-uprobes``) can look in the directory specified with
the :term:`STAGING_KERNEL_BUILDDIR` variable to find these artifacts
after the kernel has been built.
