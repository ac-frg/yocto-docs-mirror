When used by recipes that inherit the :ref:`ref-classes-setuptools3`
class, denotes the Application Binary Interface (ABI) currently in use
for Python. By default, the ABI is "m". You do not have to set this
variable as the OpenEmbedded build system sets it for you.

The OpenEmbedded build system uses the ABI to construct directory
names used when installing the Python headers and libraries in
sysroot (e.g. ``.../python3.3m/...``).
