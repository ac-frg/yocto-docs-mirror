For the BusyBox recipe, specifies whether to split the output
executable file into two parts: one for features that require
``setuid root``, and one for the remaining features (i.e. those that
do not require ``setuid root``).

The :term:`BUSYBOX_SPLIT_SUID` variable defaults to "1", which results in
splitting the output executable file. Set the variable to "0" to get
a single output executable file.
