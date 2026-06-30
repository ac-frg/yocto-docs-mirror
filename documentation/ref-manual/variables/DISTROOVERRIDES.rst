A colon-separated list of overrides specific to the current
distribution. By default, this list includes the value of
:term:`DISTRO`.

You can extend :term:`DISTROOVERRIDES` to add extra overrides that should
apply to the distribution.

The underlying mechanism behind :term:`DISTROOVERRIDES` is simply that it
is included in the default value of
:term:`OVERRIDES`.

Here is an example from :yocto_git:`meta-poky/conf/distro/poky-tiny.conf
</meta-yocto/tree/meta-poky/conf/distro/poky-tiny.conf>`::

   DISTROOVERRIDES = "poky:poky-tiny"
