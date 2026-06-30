When inheriting the :ref:`ref-classes-sbom-cve-check` class, this
variable controls whether to scan target and native, just target, or just
native recipes.

Valid values are:

-  ``target`` (default): recipes are scanned in their target context
-  ``native``: recipes are scanned in their :ref:`ref-classes-native` context
-  ``both``: recipes are scanned in both their target and
   :ref:`ref-classes-native` context
