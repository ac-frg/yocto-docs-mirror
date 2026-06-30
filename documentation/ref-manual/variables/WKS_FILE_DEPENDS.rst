When placed in the recipe that builds your image, this variable lists
build-time dependencies. The :term:`WKS_FILE_DEPENDS` variable is only
applicable when Wic images are active (i.e. when
:term:`IMAGE_FSTYPES` contains entries related
to Wic). If your recipe does not create Wic images, the variable has
no effect.

The :term:`WKS_FILE_DEPENDS` variable is similar to the
:term:`DEPENDS` variable. When you use the variable in
your recipe that builds the Wic image, dependencies you list in the
:term:`WKS_FILE_DEPENDS` variable are added to the :term:`DEPENDS` variable.

With the :term:`WKS_FILE_DEPENDS` variable, you have the possibility to
specify a list of additional dependencies (e.g. native tools,
bootloaders, and so forth), that are required to build Wic images.
Here is an example::

   WKS_FILE_DEPENDS = "some-native-tool"

In the
previous example, some-native-tool would be replaced with an actual
native tool on which the build would depend.
