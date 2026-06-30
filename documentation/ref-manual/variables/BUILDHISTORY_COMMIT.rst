When inheriting the :ref:`ref-classes-buildhistory` class, this variable
specifies whether or not to commit the build history output in a local
Git repository. If set to "1", this local repository will be maintained
automatically by the :ref:`ref-classes-buildhistory` class and a commit
will be created on every build for changes to each top-level subdirectory
of the build history output (images, packages, and sdk). If you want to
track changes to build history over time, you should set this value to
"1".

By default, the :ref:`ref-classes-buildhistory` class
enables committing the buildhistory output in a local Git repository::

   BUILDHISTORY_COMMIT ?= "1"
