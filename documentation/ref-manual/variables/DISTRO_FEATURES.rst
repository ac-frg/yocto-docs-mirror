The software support you want in your distribution for various
features. You define your distribution features in the distribution
configuration file.

In most cases, the presence or absence of a feature in
:term:`DISTRO_FEATURES` is translated to the appropriate option supplied
to the configure script during the
:term:`do_configure` task for recipes that
optionally support the feature. For example, specifying "x11" in
:term:`DISTRO_FEATURES`, causes every piece of software built for the
target that can optionally support X11 to have its X11 support
enabled.

.. note::

   Just enabling :term:`DISTRO_FEATURES` alone doesn't
   enable feature support for packages. Mechanisms such as making
   :term:`PACKAGECONFIG` track :term:`DISTRO_FEATURES` are used
   to enable/disable package features.

Two more examples are Bluetooth and NFS support. For a more complete
list of features that ships with the Yocto Project and that you can
provide with this variable, see the ":ref:`ref-features-distro`" section.
