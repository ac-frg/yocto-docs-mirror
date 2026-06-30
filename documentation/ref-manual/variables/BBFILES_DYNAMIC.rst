Activates content when identified layers are present. This mechanism
is commonly referred to as "dynamic layers". You identify the layers
by the collections that the layers define.

Use the :term:`BBFILES_DYNAMIC` variable to avoid ``.bbappend`` files
whose corresponding ``.bb`` file is in a layer that attempts to
modify other layers through ``.bbappend`` but does not want to
introduce a hard dependency on those other layers.

Use the following form for :term:`BBFILES_DYNAMIC`:
``collection_name:filename_pattern``.

The following example identifies two collection names and two
filename patterns::

   BBFILES_DYNAMIC += " \
      clang-layer:${LAYERDIR}/dynamic-layers/meta-clang/*/*/*.bbappend \
      core:${LAYERDIR}/dynamic-layers/openembedded-core/meta/*/*/*.bbappend \
      "

This next example shows an error message that occurs because invalid
entries are found, which cause parsing to fail:

.. code-block:: none

   ERROR: BBFILES_DYNAMIC entries must be of the form <collection name>:<filename pattern>, not:
       /work/my-layer/dynamic-layers/meta-security-isafw/*/*/*.bbappend
       /work/my-layer/dynamic-layers/openembedded-core/meta/*/*/*.bbappend
