When inheriting the :ref:`ref-classes-compress_doc`
class, this variable sets the compression policy used when the
OpenEmbedded build system compresses manual and info pages. By
default, the compression method used is gz (gzip). Other policies
available are xz and bz2.

For information on policies and on how to use this variable, see the
comments in the ``meta/classes-recipe/compress_doc.bbclass`` file.
