The :term:`TOOLCHAIN_NATIVE` variable can be used to override the
toolchain used by a :ref:`ref-classes-native` recipe.

The default value for this variable is the value of
:term:`PREFERRED_TOOLCHAIN` (in :ref:`ref-classes-native` contexts). See
the description of :term:`PREFERRED_TOOLCHAIN` to know the list of
possible values for :term:`TOOLCHAIN_NATIVE`.

It is possible to override the value of this variable from a recipe if
this recipe is known to support only a specific toolchain.
