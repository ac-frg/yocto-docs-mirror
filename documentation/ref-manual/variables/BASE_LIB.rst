The library directory name for the CPU or Application Binary
Interface (ABI) tune. The :term:`BASE_LIB` applies only in the Multilib
context. See the ":ref:`dev-manual/libraries:combining multiple versions of library files into one image`"
section in the Yocto Project Development Tasks Manual for information
on Multilib.

The :term:`BASE_LIB` variable is defined in the machine include files in
:term:`OpenEmbedded-Core (OE-Core)`. If Multilib is not
being used, the value defaults to "lib".
