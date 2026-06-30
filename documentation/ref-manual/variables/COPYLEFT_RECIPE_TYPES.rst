A space-separated list of recipe types to include in the source
archived by the :ref:`archiver <ref-classes-archiver>` class.
Recipe types are ``target``, :ref:`ref-classes-native`,
:ref:`ref-classes-nativesdk`, :ref:`ref-classes-cross`,
:ref:`ref-classes-crosssdk`, and :ref:`ref-classes-cross-canadian`.

The default value, which is "target*", for :term:`COPYLEFT_RECIPE_TYPES`
is set by the :ref:`ref-classes-copyleft_filter` class, which is
inherited by the :ref:`ref-classes-archiver` class.
