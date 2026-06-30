A colon-separated list of overrides that apply to the current
machine. By default, this list includes the value of
:term:`MACHINE`.

You can extend :term:`MACHINEOVERRIDES` to add extra overrides that
should apply to a machine. For example, all machines emulated in QEMU
(e.g. ``qemuarm``, ``qemux86``, and so forth) include a file named
``meta/conf/machine/include/qemu.inc`` that prepends the following
override to :term:`MACHINEOVERRIDES`::

   MACHINEOVERRIDES =. "qemuall:"

This
override allows variables to be overridden for all machines emulated
in QEMU, like in the following example from the ``connman-conf``
recipe::

   SRC_URI:append:qemuall = " file://wired.config \
       file://wired-setup \
       "

The underlying mechanism behind
:term:`MACHINEOVERRIDES` is simply that it is included in the default
value of :term:`OVERRIDES`.
