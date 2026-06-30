This variable points to a directory were BitBake places temporary
files, which consist mostly of task logs and scripts, when building a
particular recipe. The variable is typically set as follows::

   T = "${WORKDIR}/temp"

The :term:`WORKDIR` is the directory into which
BitBake unpacks and builds the recipe. The default ``bitbake.conf``
file sets this variable.

The :term:`T` variable is not to be confused with the
:term:`TMPDIR` variable, which points to the root of
the directory tree where BitBake places the output of an entire
build.
