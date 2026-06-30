This is a specific kernel compiler flag for a CPU or Application
Binary Interface (ABI) tune. The flag is used rarely and only for
cases where a userspace :term:`TUNE_CCARGS` is not
compatible with the kernel compilation. The :term:`TARGET_CC_KERNEL_ARCH`
variable allows the kernel (and associated modules) to use a
different configuration. See the
``meta/conf/machine/include/arm/feature-arm-thumb.inc`` file in
:term:`OpenEmbedded-Core (OE-Core)` for an example.
