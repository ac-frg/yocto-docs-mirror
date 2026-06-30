Specifies the path to the sysroot used for the system for which the
component generates code. For components that do not generate code,
which is the majority, :term:`STAGING_DIR_TARGET` is set to match
:term:`STAGING_DIR_HOST`.

Some recipes build binaries that can run on the target system but those
binaries in turn generate code for another different system (e.g.
:ref:`ref-classes-cross-canadian` recipes). Using terminology from GNU,
the primary system is referred to as the "HOST" and the secondary, or
different, system is referred to as the "TARGET". Thus, the binaries
run on the "HOST" system and generate binaries for the "TARGET"
system. The :term:`STAGING_DIR_HOST` variable points to the sysroot used
for the "HOST" system, while :term:`STAGING_DIR_TARGET` points to the
sysroot used for the "TARGET" system.
