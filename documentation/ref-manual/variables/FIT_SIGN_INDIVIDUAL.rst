If set to "1", the :ref:`ref-classes-kernel-fit-image` class signs each
image node individually, including the kernel, DTB, RAM disk, and any
other image types present in the FIT image, in addition to signing the
configuration nodes.
This can be useful if you need to verify signatures outside of the
U-Boot boot process. By default, this variable is set to "0".

If :term:`UBOOT_SIGN_ENABLE` is set to "1" and
:term:`FIT_SIGN_INDIVIDUAL` remains at its default value of "0", only the
configuration nodes are signed. Since configuration nodes include hashes
of their referenced image nodes, the integrity of the entire FIT image is
ensured as long as the image nodes are loaded via the configuration nodes
and the hashes of the image nodes are checked. That's usually the case.

Enabling :term:`FIT_SIGN_INDIVIDUAL` typically increases complexity for
little benefit. There might be exceptions such as image nodes that are
not referenced by any configuration node or loaded directly for whatever
reason.
For most use cases, setting this variable to "0" provides sufficient
security.

For further details, refer to the official U-Boot documentation:
`U-Boot fit signature <https://docs.u-boot.org/en/latest/usage/fit/signature.html>`__
and more specifically at:
`U-Boot signed configurations <https://docs.u-boot.org/en/latest/usage/fit/signature.html#signed-configurations>`__.

Signing only the image nodes is intentionally not implemented by
:term:`OpenEmbedded-Core (OE-Core)`, as it is vulnerable to mix-and-match
attacks.
