This variable, used by the ``psplash`` recipe, allows to customize
the default splashscreen image.

Specified images in PNG format are converted to ``.h`` files by the recipe,
and are included in the ``psplash`` binary, so you won't find them in
the root filesystem.

To make such a change, it is recommended to customize the
``psplash`` recipe in a custom layer. Here is an example structure for
an ``ACME`` board::

    meta-acme/recipes-core/psplash
    ├── files
    │   └── logo-acme.png
    └── psplash_%.bbappend

And here are the contents of the ``psplash_%.bbappend`` file in
this example::

    SPLASH_IMAGES = "file://logo-acme.png;outsuffix=default"
    FILESEXTRAPATHS:prepend := "${THISDIR}/files:"

You could even add specific configuration options for ``psplash``,
for example::

    EXTRA_OECONF += "--disable-startup-msg --enable-img-fullscreen"

For information on append files, see the
":ref:`dev-manual/layers:appending other layers metadata with your layer`"
section.
