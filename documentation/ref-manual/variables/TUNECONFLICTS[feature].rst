Specifies CPU or Application Binary Interface (ABI) tuning features
that conflict with feature.

Known tuning conflicts are specified in the machine include files in
:term:`OpenEmbedded-Core (OE-Core)`. Here is an example from
the ``meta/conf/machine/include/mips/arch-mips.inc`` include file
that lists the "o32" and "n64" features as conflicting with the "n32"
feature::

   TUNECONFLICTS[n32] = "o32 n64"
