When inheriting the :ref:`ref-classes-buildhistory`
class, this variable specifies the directory in which build history
information is kept. For more information on how the variable works,
see the :ref:`ref-classes-buildhistory` class.

By default, the :ref:`ref-classes-buildhistory` class sets the directory
as follows::

   BUILDHISTORY_DIR ?= "${TOPDIR}/buildhistory"
