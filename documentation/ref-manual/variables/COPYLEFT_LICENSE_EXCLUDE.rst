A space-separated list of licenses to exclude from the source archived by
the :ref:`ref-classes-archiver` class. In other words, if a license in a
recipe's :term:`LICENSE` value is in the value of
:term:`COPYLEFT_LICENSE_EXCLUDE`, then its source is not archived by the
class.

.. note::

   The :term:`COPYLEFT_LICENSE_EXCLUDE` variable takes precedence over the
   :term:`COPYLEFT_LICENSE_INCLUDE` variable.

The default value, which is "CLOSED Proprietary", for
:term:`COPYLEFT_LICENSE_EXCLUDE` is set by the
:ref:`ref-classes-copyleft_filter` class, which
is inherited by the :ref:`ref-classes-archiver` class.
