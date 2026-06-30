When the :ref:`ref-classes-debian` class is inherited,
which is the default behavior, :term:`DEBIAN_NOAUTONAME` specifies a
particular package should not be renamed according to Debian library
package naming. You must use the package name as an override when you
set this variable. Here is an example from the ``fontconfig`` recipe::

   DEBIAN_NOAUTONAME:fontconfig-utils = "1"
