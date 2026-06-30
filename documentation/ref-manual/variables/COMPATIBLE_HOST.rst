A regular expression that resolves to one or more hosts (when the
recipe is native) or one or more targets (when the recipe is
non-native) with which a recipe is compatible. The regular expression
is matched against :term:`HOST_SYS`. You can use the
variable to stop recipes from being built for classes of systems with
which the recipes are not compatible. Stopping these builds is
particularly useful with kernels. The variable also helps to increase
parsing speed since the build system skips parsing recipes not
compatible with the current system.
