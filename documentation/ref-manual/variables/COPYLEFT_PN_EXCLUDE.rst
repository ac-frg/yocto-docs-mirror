A list of recipes to exclude in the source archived by the
:ref:`ref-classes-archiver` class. The :term:`COPYLEFT_PN_EXCLUDE`
variable overrides the license inclusion and exclusion caused through the
:term:`COPYLEFT_LICENSE_INCLUDE` and :term:`COPYLEFT_LICENSE_EXCLUDE`
variables, respectively.

The default value, which is "" indicating to not explicitly exclude
any recipes by name, for :term:`COPYLEFT_PN_EXCLUDE` is set by the
:ref:`ref-classes-copyleft_filter` class, which is inherited by the
:ref:`ref-classes-archiver` class.
