Monitors disk space and available inodes during the build and allows
you to control the build based on these parameters.

Disk space monitoring is disabled by default. To enable monitoring,
add the :term:`BB_DISKMON_DIRS` variable to your ``conf/local.conf`` file
found in the :term:`Build Directory`. Use the
following form:

.. code-block:: none

   BB_DISKMON_DIRS = "action,dir,threshold [...]"

   where:

      action is:
         ABORT:     Immediately stop the build when
                    a threshold is broken.
         STOPTASKS: Stop the build after the currently
                    executing tasks have finished when
                    a threshold is broken.
         WARN:      Issue a warning but continue the
                    build when a threshold is broken.
                    Subsequent warnings are issued as
                    defined by the BB_DISKMON_WARNINTERVAL
                    variable, which must be defined in
                    the conf/local.conf file.

      dir is:
         Any directory you choose. You can specify one or
         more directories to monitor by separating the
         groupings with a space.  If two directories are
         on the same device, only the first directory
         is monitored.

      threshold is:
         Either the minimum available disk space,
         the minimum number of free inodes, or
         both.  You must specify at least one.  To
         omit one or the other, simply omit the value.
         Specify the threshold using G, M, K for Gbytes,
         Mbytes, and Kbytes, respectively. If you do
         not specify G, M, or K, Kbytes is assumed by
         default.  Do not use GB, MB, or KB.

Here are some examples::

   BB_DISKMON_DIRS = "ABORT,${TMPDIR},1G,100K WARN,${SSTATE_DIR},1G,100K"
   BB_DISKMON_DIRS = "STOPTASKS,${TMPDIR},1G"
   BB_DISKMON_DIRS = "ABORT,${TMPDIR},,100K"

The first example works only if you also provide the
:term:`BB_DISKMON_WARNINTERVAL`
variable in the ``conf/local.conf``. This example causes the build
system to immediately stop when either the disk space in
``${TMPDIR}`` drops below 1 Gbyte or the available free inodes drops
below 100 Kbytes. Because two directories are provided with the
variable, the build system also issue a warning when the disk space
in the ``${SSTATE_DIR}`` directory drops below 1 Gbyte or the number
of free inodes drops below 100 Kbytes. Subsequent warnings are issued
during intervals as defined by the :term:`BB_DISKMON_WARNINTERVAL`
variable.

The second example stops the build after all currently executing
tasks complete when the minimum disk space in the ``${TMPDIR}``
directory drops below 1 Gbyte. No disk monitoring occurs for the free
inodes in this case.

The final example immediately stops the build when the number of
free inodes in the ``${TMPDIR}`` directory drops below 100 Kbytes. No
disk space monitoring for the directory itself occurs in this case.
