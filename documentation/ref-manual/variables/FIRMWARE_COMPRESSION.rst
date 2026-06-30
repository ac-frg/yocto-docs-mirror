The :term:`FIRMWARE_COMPRESSION` allows compressing the firmware provided
by the ``linux-firmware`` recipe. The default value of this variable is an
empty string (no compression), and the possible values it can take are
``xz`` and ``zst``. This can allow significant disk space savings.

For this to work, the Linux Kernel requires the
``CONFIG_FW_LOADER_COMPRESS_XZ`` or ``CONFIG_FW_LOADER_COMPRESS_ZSTD``
configuration options to be set.
