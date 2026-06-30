Allows you to extend a recipe so that it builds variants of the
software. There are common variants for recipes as "natives" like
``quilt-native``, which is a copy of Quilt built to run on the build
system; "crosses" such as ``gcc-cross``, which is a compiler built to
run on the build machine but produces binaries that run on the target
:term:`MACHINE`; ":ref:`ref-classes-nativesdk`", which
targets the SDK machine instead of :term:`MACHINE`; and "mulitlibs" in
the form "``multilib:``\ multilib_name".

To build a different variant of the recipe with a minimal amount of
code, it usually is as simple as adding the following to your recipe::

   BBCLASSEXTEND =+ "native nativesdk"
   BBCLASSEXTEND =+ "multilib:multilib_name"

.. note::

   Internally, the :term:`BBCLASSEXTEND` mechanism generates recipe
   variants by rewriting variable values and applying overrides such
   as ``:class-native``. For example, to generate a native version of
   a recipe, a :term:`DEPENDS` on "foo" is rewritten
   to a :term:`DEPENDS` on "foo-native".

   Even when using :term:`BBCLASSEXTEND`, the recipe is only parsed once.
   Parsing once adds some limitations. For example, it is not
   possible to include a different file depending on the variant,
   since ``include`` statements are processed when the recipe is
   parsed.
