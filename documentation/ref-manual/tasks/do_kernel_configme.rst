After the kernel is patched by the :term:`do_patch`
task, the :term:`do_kernel_configme` task assembles and merges all the
kernel config fragments into a merged configuration that can then be
passed to the kernel configuration phase proper. This is also the time
during which user-specified defconfigs are applied if present, and where
configuration modes such as ``--allnoconfig`` are applied.
