The :term:`SSTATE_SKIP_CREATION` variable can be used to skip the
creation of :ref:`shared state <overview-manual/concepts:shared state cache>`
tarball files. It makes sense e.g. for image creation tasks as tarring images
and keeping them in sstate would consume a lot of disk space.

In general it is not recommended to use this variable as missing sstate
artefacts adversely impact the build, particularly for entries in the
middle of dependency chains. The case it can make sense is where the
size and time costs of the artefact are similar to just running the
tasks. This generally only applies to end artefact output like images.

The syntax to disable it for one task is::

   SSTATE_SKIP_CREATION:task-image-complete = "1"

The syntax to disable it for the whole recipe is::

   SSTATE_SKIP_CREATION = "1"
