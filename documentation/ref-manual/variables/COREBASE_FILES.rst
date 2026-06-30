Lists files from the :term:`COREBASE` directory that
should be copied other than the layers listed in the
``bblayers.conf`` file. The :term:`COREBASE_FILES` variable allows
to copy metadata from the OpenEmbedded build system
into the extensible SDK.

Explicitly listing files in :term:`COREBASE` is needed because it
typically contains build directories and other files that should not
normally be copied into the extensible SDK. Consequently, the value
of :term:`COREBASE_FILES` is used in order to only copy the files that
are actually needed.
