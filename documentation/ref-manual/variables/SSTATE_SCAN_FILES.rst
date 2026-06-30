Controls the list of files the OpenEmbedded build system scans for
hardcoded installation paths. The variable uses a space-separated
list of filenames (not paths) with standard wildcard characters
allowed.

During a build, the OpenEmbedded build system creates a shared state
(sstate) object during the first stage of preparing the sysroots.
That object is scanned for hardcoded paths for original installation
locations. The list of files that are scanned for paths is controlled
by the :term:`SSTATE_SCAN_FILES` variable. Typically, recipes add files
they want to be scanned to the value of :term:`SSTATE_SCAN_FILES` rather
than the variable being comprehensively set. The
:ref:`ref-classes-sstate` class specifies the default list of files.

For details on the process, see the :ref:`ref-classes-staging` class.
