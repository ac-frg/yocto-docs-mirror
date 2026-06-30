When inheriting the :ref:`ref-classes-buildhistory`
class, this variable specifies a common path prefix that should be
stripped off the beginning of paths in the task signature list when the
``task`` feature is active in :term:`BUILDHISTORY_FEATURES`. This can be
useful when build history is populated from multiple sources that may not
all use the same top level directory.

By default, the :ref:`ref-classes-buildhistory` class sets the variable
as follows::

   BUILDHISTORY_PATH_PREFIX_STRIP ?= ""

In this case, no prefixes will be stripped.
