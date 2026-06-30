Specifies the packages that should be installed to provide an X
server and drivers for the current machine, assuming your image
directly includes ``packagegroup-core-x11-xserver`` or, perhaps
indirectly, includes "x11-base" in
:term:`IMAGE_FEATURES`.

The default value of :term:`XSERVER`, if not specified in the machine
configuration, is "xserver-xorg xf86-video-fbdev xf86-input-evdev".
