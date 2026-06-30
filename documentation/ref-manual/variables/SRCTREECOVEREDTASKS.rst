A list of tasks that are typically not relevant (and therefore skipped)
when building using the :ref:`ref-classes-externalsrc`
class. The default value as set in that class file is the set of tasks
that are rarely needed when using external source::

   SRCTREECOVEREDTASKS ?= "do_patch do_unpack do_fetch"

The notable exception is when processing external kernel source as
defined in the :ref:`ref-classes-kernel-yocto` class file (formatted for
aesthetics)::

   SRCTREECOVEREDTASKS += "\
     do_validate_branches \
     do_kernel_configcheck \
     do_kernel_checkout \
     do_fetch \
     do_unpack \
     do_patch \
   "

See the associated :term:`EXTERNALSRC` and :term:`EXTERNALSRC_BUILD`
variables for more information.
