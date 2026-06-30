The :term:`TOOLCHAIN` variable can be used to override the toolchain used
by a recipe.

The default value for this variable is the value of
:term:`PREFERRED_TOOLCHAIN`. See the description of
:term:`PREFERRED_TOOLCHAIN` to know the list of possible values for
:term:`TOOLCHAIN`.

It is possible to override the value of this variable from a recipe if
this recipe is known to support only a specific toolchain. For example,
the :oe_git:`Pseudo </openembedded-core/tree/meta/recipes-devtools/pseudo/pseudo_git.bb>`
recipe overrides this variable to "gcc", because Pseudo uses GCC compiler
built-ins options that the Clang/LLVM compiler does not provide.
