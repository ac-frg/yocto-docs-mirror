This variable allows to set the default unit that systemd starts at bootup.
Usually, this is either ``multi-user.target`` or ``graphical.target``.
This works by creating a ``default.target`` symbolic link to the chosen systemd
target file.

See `systemd's documentation
<https://www.freedesktop.org/software/systemd/man/systemd.special.html>`__
for details.

For example, this variable is used in the :oe_git:`core-image-minimal-xfce.bb
</meta-openembedded/tree/meta-xfce/recipes-core/images/core-image-minimal-xfce.bb>`
recipe::

    SYSTEMD_DEFAULT_TARGET = "graphical.target"
