Specifies the method for handling FPU code. For FPU-less targets,
which include most ARM CPUs, the variable must be set to "soft". If
not, the kernel emulation gets used, which results in a performance
penalty.
