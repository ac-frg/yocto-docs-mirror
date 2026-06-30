Specifies a valid CPU or Application Binary Interface (ABI) tuning
feature. The specified feature is stored as a flag. Valid features
are specified in the machine include files (e.g.
``meta/conf/machine/include/arm/arch-arm.inc``). Here is an example
from that file::

   TUNEVALID[bigendian] = "Enable big-endian mode."

See the machine include files in :term:`OpenEmbedded-Core (OE-Core)`
for these features.
