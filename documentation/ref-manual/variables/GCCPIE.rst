Enables Position Independent Executables (PIE) within the GNU C
Compiler (GCC). Enabling PIE in the GCC makes Return Oriented
Programming (ROP) attacks much more difficult to execute.

By default the ``security_flags.inc`` file enables PIE by setting the
variable as follows::

   GCCPIE ?= "--enable-default-pie"
