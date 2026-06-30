A list of additional features to include in an image. When listing
more than one feature, separate them with a space.

Typically, you configure this variable in your ``local.conf`` file,
which is found in the :term:`Build Directory`. Although you can use this
variable from within a recipe, best practices dictate that you do not.

.. note::

   To enable primary features from within the image recipe, use the
   :term:`IMAGE_FEATURES` variable.

Here are some examples of features you can add:

  - "dbg-pkgs" --- adds -dbg packages for all installed packages including
    symbol information for debugging and profiling.

  - "empty-root-password" --- This feature can be used if you want to
    allow root login with an empty password.
  - "allow-empty-password" --- Allows Dropbear and OpenSSH to accept
    logins from accounts having an empty password string.
  - "allow-root-login" --- Allows Dropbear and OpenSSH to accept root logins.
  - "post-install-logging" --- Enables logging postinstall script runs to
    the ``/var/log/postinstall.log`` file on first boot of the image on
    the target system.
  - "dev-pkgs" --- adds -dev packages for all installed packages. This is
    useful if you want to develop against the libraries in the image.
  - "read-only-rootfs" --- creates an image whose root filesystem is
    read-only. See the
    ":ref:`security-manual/read-only-rootfs:creating a read-only root filesystem`"
    section in the Yocto Project Development Tasks Manual for more
    information
  - "tools-debug" --- adds debugging tools such as gdb and strace.
  - "tools-sdk" --- adds development tools such as gcc, make,
    pkgconfig and so forth.
  - "tools-testapps" --- adds useful testing tools
    such as ts_print, aplay, arecord and so forth.

For a complete list of image features that ships with the Yocto
Project, see the ":ref:`ref-features-image`" section.

For an example that shows how to customize your image by using this
variable, see the ":ref:`dev-manual/customizing-images:customizing images using custom \`\`image_features\`\` and \`\`extra_image_features\`\``"
section in the Yocto Project Development Tasks Manual.
