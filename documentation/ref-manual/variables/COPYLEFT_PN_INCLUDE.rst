A list of recipes to include in the source archived by the
:ref:`ref-classes-archiver` class. The :term:`COPYLEFT_PN_INCLUDE`
variable overrides the license inclusion and exclusion caused through the
:term:`COPYLEFT_LICENSE_INCLUDE` and :term:`COPYLEFT_LICENSE_EXCLUDE`
variables, respectively.

The default value, which is "" indicating to not explicitly include
any recipes by name, for :term:`COPYLEFT_PN_INCLUDE` is set by the
:ref:`ref-classes-copyleft_filter` class, which is inherited by the
:ref:`ref-classes-archiver` class.
