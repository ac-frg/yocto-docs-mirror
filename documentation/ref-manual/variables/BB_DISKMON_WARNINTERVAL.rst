Defines the disk space and free inode warning intervals. To set these
intervals, define the variable in your ``conf/local.conf`` file in
the :term:`Build Directory`.

If you are going to use the :term:`BB_DISKMON_WARNINTERVAL` variable, you
must also use the :term:`BB_DISKMON_DIRS`
variable and define its action as "WARN". During the build,
subsequent warnings are issued each time disk space or number of free
inodes further reduces by the respective interval.

If you do not provide a :term:`BB_DISKMON_WARNINTERVAL` variable and you
do use :term:`BB_DISKMON_DIRS` with the "WARN" action, the disk
monitoring interval defaults to the following::

   BB_DISKMON_WARNINTERVAL = "50M,5K"

When specifying the variable in your configuration file, use the
following form:

.. code-block:: none

   BB_DISKMON_WARNINTERVAL = "disk_space_interval,disk_inode_interval"

   where:

      disk_space_interval is:
         An interval of memory expressed in either
         G, M, or K for Gbytes, Mbytes, or Kbytes,
         respectively. You cannot use GB, MB, or KB.

      disk_inode_interval is:
         An interval of free inodes expressed in either
         G, M, or K for Gbytes, Mbytes, or Kbytes,
         respectively. You cannot use GB, MB, or KB.

Here is an example::

   BB_DISKMON_DIRS = "WARN,${SSTATE_DIR},1G,100K"
   BB_DISKMON_WARNINTERVAL = "50M,5K"

These variables cause the
OpenEmbedded build system to issue subsequent warnings each time the
available disk space further reduces by 50 Mbytes or the number of
free inodes further reduces by 5 Kbytes in the ``${SSTATE_DIR}``
directory. Subsequent warnings based on the interval occur each time
a respective interval is reached beyond the initial warning (i.e. 1
Gbytes and 100 Kbytes).
