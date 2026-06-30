Specifies the system init manager to use. Available options are:

-  ``sysvinit``
-  ``systemd``
-  ``mdev-busybox``

With ``sysvinit``, the init manager is set to
:wikipedia:`SysVinit <Init#SysV-style>`, the traditional UNIX init
system. This is the default choice in the :term:`Poky` distribution, together with
the Udev device manager (see the ":ref:`device-manager`" section).

With ``systemd``, the init manager becomes :wikipedia:`systemd <Systemd>`,
which comes with the :wikipedia:`udev <Udev>` device manager.

With ``mdev-busybox``, the init manager becomes the much simpler BusyBox
init, together with the BusyBox mdev device manager. This is the simplest
and lightest solution, and probably the best choice for low-end systems
with a rather slow CPU and a limited amount of RAM.

More concretely, this is used to include
``conf/distro/include/init-manager-${INIT_MANAGER}.inc`` into the global
configuration. You can have a look at the
:oe_git:`meta/conf/distro/include/init-manager-*.inc </openembedded-core/tree/meta/conf/distro/include>`
files for more information, and also the ":ref:`init-manager`"
section in the Yocto Project Development Tasks Manual.
