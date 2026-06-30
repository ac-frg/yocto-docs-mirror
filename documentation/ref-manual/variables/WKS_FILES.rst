Specifies a list of candidate Wic kickstart files to be used by the
OpenEmbedded build system to create a partitioned image. Only the
first one that is found, from left to right, will be used.

This is only useful when there are multiple ``.wks`` files that can be
used to produce an image. A typical case is when multiple layers are
used for different hardware platforms, each supplying a different
``.wks`` file. In this case, you specify all possible ones through
:term:`WKS_FILES`.

If only one ``.wks`` file is used, set :term:`WKS_FILE` instead.
