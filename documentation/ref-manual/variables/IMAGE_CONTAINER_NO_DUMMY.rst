When an image recipe has the ``container`` image type in
:term:`IMAGE_FSTYPES`, it expects the :term:`PREFERRED_PROVIDER` for
the Linux kernel (``virtual/kernel``) to be set to ``linux-dummy`` from a
:term:`configuration file`. Otherwise, an error is triggered.

When set to "1", the :term:`IMAGE_CONTAINER_NO_DUMMY` variable allows the
:term:`PREFERRED_PROVIDER` variable to be set to another value, thus
skipping the check and not triggering the build error. Any other value
will keep the check.

This variable should be set from the image recipe using the ``container``
image type.

See the documentation of the :ref:`ref-classes-image-container` class for
more information on why setting the :term:`PREFERRED_PROVIDER` to
``linux-dummy`` is advised with this class.
