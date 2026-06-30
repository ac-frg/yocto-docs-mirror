Determines the action to take when a patch fails. You can set this
variable to one of two values: "noop" and "user".

The default value of "noop" causes the build to simply fail when the
OpenEmbedded build system cannot successfully apply a patch. Setting
the value to "user" causes the build system to launch a shell and
places you in the right location so that you can manually resolve the
conflicts.

Set this variable in your ``local.conf`` file.
