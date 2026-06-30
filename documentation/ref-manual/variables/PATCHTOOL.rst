Specifies the utility used to apply patches for a recipe during the
:term:`do_patch` task. You can specify one of
three utilities: "patch", "quilt", or "git". The default utility used
is "quilt" except for the quilt-native recipe itself. Because the
quilt tool is not available at the time quilt-native is being
patched, it uses "patch".

If you wish to use an alternative patching tool, set the variable in
the recipe using one of the following::

   PATCHTOOL = "patch"
   PATCHTOOL = "quilt"
   PATCHTOOL = "git"
