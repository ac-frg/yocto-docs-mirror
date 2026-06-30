If set, locale names are renamed such that those lacking an explicit
encoding (e.g. ``en_US``) will always be UTF-8, and non-UTF-8 encodings
are renamed to, e.g., ``en_US.ISO-8859-1``. Otherwise, the encoding is
specified by `Glibc`'s ``SUPPORTED`` file. This is not supported for
pre-compiled locales.
