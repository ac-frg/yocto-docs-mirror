Specifies whether the data referenced through
:term:`PKGDATA_DIR` is needed or not.
:term:`KERNELDEPMODDEPEND` does not control whether or not that data
exists, but simply whether or not it is used. If you do not need to
use the data, set the :term:`KERNELDEPMODDEPEND` variable in your
:term:`Initramfs` recipe. Setting the variable there when the data is not
needed avoids a potential dependency loop.
