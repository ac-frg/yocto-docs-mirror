A space-separated list of files installed into the extra partition(s)
when preparing an image using the Wic tool with the
``extra_partition`` source plugin. By default,
the files are
installed under the same name as the source files. To change the
installed name, separate it from the original name with a semi-colon
(;). Source files need to be located in
:term:`DEPLOY_DIR_IMAGE`. Here is an
example::

   IMAGE_EXTRA_PARTITION_FILES = "foobar file.conf;config"

In the above example, the file ``foobar`` is installed with its original name
``foobar``, while the file ``file.conf`` is installed and renamed to ``config``.

Alternatively, source files can be picked up using a glob pattern.
However, hidden files are ignored, and the pattern is non-recursive
(subdirectories are ignored).
The destination file will have the same name as the base
name of the source file path. To install files into a renamed directory
within the target location, pass its name after a semi-colon (;).
Here are two examples::

   IMAGE_EXTRA_PARTITION_FILES = "foo/*"
   IMAGE_EXTRA_PARTITION_FILES = "foo/*;bar/"

The first line in this example
installs all files from ``foo`` directory
into the root of the target partition. The second line in this example installs
the same files into a ``bar`` directory within the target partition.
The ``bar/`` directory is automatically created if it does not exist.

You can also specify the target by label, UUID or partition name if multiple
extra partitions coexist. Let's take the following example. This would be
the WKS file for the image currently being built::

   part --source extra_partition --fstype=ext4 --label foo
   part --source extra_partition --fstype=ext4 --uuid e7d0824e-cda3-4bed-9f54-9ef5312d105d
   part --source extra_partition --fstype=ext4 --part-name config

And the following configuration::

   IMAGE_EXTRA_PARTITION_FILES_label-foo = "foo/*"
   IMAGE_EXTRA_PARTITION_FILES_uuid-e7d0824e-cda3-4bed-9f54-9ef5312d105d = "foo/*;bar/"
   IMAGE_EXTRA_PARTITION_FILES_part-name-config = "config"

Then:

-  The partition labeled "foo" would get all files from the ``foo``
   directory.

-  The partition whose UUID is "e7d0824e-cda3-4bed-9f54-9ef5312d105d"
   would get all files from the ``foo`` directory, installed into a
   ``bar`` directory.

-  The partition named "config" would get the file ``config``.

You can find information on how to use the Wic tool in the
":ref:`dev-manual/wic:creating partitioned images using wic`"
section of the Yocto Project Development Tasks Manual. Reference
material for Wic is located in the
":doc:`/ref-manual/kickstart`" chapter.
