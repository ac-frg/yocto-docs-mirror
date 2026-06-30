This variable controls the toolchain used for compiling recipes in the
architecture of the target :term:`MACHINE`.

There are two possible values for this variable at the moment:

-  :ref:`gcc <ref-classes-toolchain-gcc>` (default): the GCC/Binutils toolchain.
-  :ref:`clang <ref-classes-toolchain-clang>`: the Clang/LLVM toolchain.

:term:`PREFERRED_TOOLCHAIN_TARGET` will make the :ref:`ref-classes-base`
class inherit one of the toolchain classes defined in
:oe_git:`meta/classes/toolchain
</openembedded-core/tree/meta/classes/toolchain>`. As a consequence, this
variable should be set globally from a :term:`configuration file`.

These classes define commands used for cross-compiling such as :term:`CC`,
:term:`CXX`, :term:`LD` and so on.

A recipe that does not support the toolchain specified by
:term:`PREFERRED_TOOLCHAIN_TARGET` can override it locally with
:term:`TOOLCHAIN`.
