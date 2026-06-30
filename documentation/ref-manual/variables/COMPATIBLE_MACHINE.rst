A regular expression that resolves to one or more target machines
with which a recipe is compatible. The regular expression is matched
against :term:`MACHINEOVERRIDES`. You can use
the variable to stop recipes from being built for machines with which
the recipes are not compatible. Stopping these builds is particularly
useful with kernels. The variable also helps to increase parsing
speed since the build system skips parsing recipes not compatible
with the current machine.

If one wants to have a recipe only available for some architectures
(here ``aarch64`` and ``mips64``), the following can be used::

   COMPATIBLE_MACHINE = "^$"
   COMPATIBLE_MACHINE:arch64 = "^(aarch64)$"
   COMPATIBLE_MACHINE:mips64 = "^(mips64)$"

The first line means "match all machines whose :term:`MACHINEOVERRIDES`
contains the empty string", which will always be none.

The second is for matching all machines whose :term:`MACHINEOVERRIDES`
contains one override which is exactly ``aarch64``.

The third is for matching all machines whose :term:`MACHINEOVERRIDES`
contains one override which is exactly ``mips64``.

The same could be achieved with::

   COMPATIBLE_MACHINE = "^(aarch64|mips64)$"

.. note::

   When :term:`COMPATIBLE_MACHINE` is set in a native recipe,
   the recipe is always skipped. All native recipes must be
   entirely target independent and should not rely on :term:`MACHINE`.
