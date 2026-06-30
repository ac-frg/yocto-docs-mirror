After the kernel has been compiled but before the kernel modules have
been compiled, this task copies files required for module builds and
which are generated from the kernel build into the shared work
directory. With these copies successfully copied, the
:term:`do_compile_kernelmodules` task
can successfully build the kernel modules in the next step of the build.
