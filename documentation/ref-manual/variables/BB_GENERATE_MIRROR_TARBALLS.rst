Causes tarballs of the source control repositories (e.g. Git
repositories), including metadata, to be placed in the
:term:`DL_DIR` directory.

For performance reasons, creating and placing tarballs of these
repositories is not the default action by the OpenEmbedded build
system::

   BB_GENERATE_MIRROR_TARBALLS = "1"

Set this variable in your
``local.conf`` file in the :term:`Build Directory`.

Once you have the tarballs containing your source files, you can
clean up your :term:`DL_DIR` directory by deleting any Git or other
source control work directories.
