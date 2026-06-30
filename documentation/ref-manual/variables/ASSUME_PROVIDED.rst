Lists recipe names (:term:`PN` values) BitBake does not
attempt to build. Instead, BitBake assumes these recipes have already
been built.

In OpenEmbedded-Core, :term:`ASSUME_PROVIDED` mostly specifies native
tools that should not be built. An example is ``git-native``, which
when specified, allows for the Git binary from the host to be used
rather than building ``git-native``.
