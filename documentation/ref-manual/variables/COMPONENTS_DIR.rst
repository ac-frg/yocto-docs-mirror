Stores sysroot components provided by each recipe. The OpenEmbedded build
system uses :term:`COMPONENTS_DIR` when constructing recipe-specific
sysroots for other recipes.

The default is
"``${``\ :term:`STAGING_DIR`\ ``}-components``."
(i.e.
"``${``\ :term:`TMPDIR`\ ``}/sysroots-components``").
