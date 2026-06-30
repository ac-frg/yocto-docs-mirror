A space-separated list of licenses to include in the source archived
by the :ref:`ref-classes-archiver` class. In other
words, if a license in a recipe's :term:`LICENSE`
value is in the value of :term:`COPYLEFT_LICENSE_INCLUDE`, then its
source is archived by the class.

The default value is set by the :ref:`ref-classes-copyleft_filter` class,
which is inherited by the :ref:`ref-classes-archiver` class. The default
value includes "GPL*", "LGPL*", and "AGPL*".
