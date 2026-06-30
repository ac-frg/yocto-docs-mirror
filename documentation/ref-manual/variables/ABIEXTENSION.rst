Extension to the Application Binary Interface (ABI) field of the GNU
canonical architecture name (e.g. "eabi").

ABI extensions are set in the machine include files. For example, the
``meta/conf/machine/include/arm/arch-arm.inc`` file sets the
following extension::

   ABIEXTENSION = "eabi"
