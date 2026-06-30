When inheriting the :ref:`ref-classes-buildhistory`
class, this variable specifies the build history features to be
enabled. For more information on how build history works, see the
":ref:`dev-manual/build-quality:maintaining build output quality with \`\`buildhistory\`\``"
section in the Yocto Project Development Tasks Manual.

You can specify these features in the form of a space-separated list:

-  *image:* Analysis of the contents of images, which includes the
   list of installed packages among other things.

-  *package:* Analysis of the contents of individual packages.

-  *sdk:* Analysis of the contents of the software development kit
   (SDK).

-  *task:* Save output file signatures for
   :ref:`shared state <overview-manual/concepts:shared state cache>`
   (sstate) tasks.
   This saves one file per task and lists the SHA-256 checksums for
   each file staged (i.e. the output of the task).

By default, the :ref:`ref-classes-buildhistory` class enables the
following features::

   BUILDHISTORY_FEATURES ?= "image package sdk"
