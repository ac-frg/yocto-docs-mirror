Defines the maximum allowed size of the generated image in kilobytes.
The build will fail if the generated image size exceeds this value.

The generated image size undergoes several calculation steps before being
compared to :term:`IMAGE_ROOTFS_MAXSIZE`.
In the first step, the size of the directory pointed to by :term:`IMAGE_ROOTFS`
is calculated.
In the second step, the result from the first step is multiplied
by :term:`IMAGE_OVERHEAD_FACTOR`.
In the third step, the result from the second step is compared with
:term:`IMAGE_ROOTFS_SIZE`. The larger value of these is added to
:term:`IMAGE_ROOTFS_EXTRA_SPACE`.
In the fourth step, the result from the third step is checked for
a decimal part. If it has one, it is rounded up to the next integer.
If it does not, it is simply converted into an integer.
In the fifth step, the :term:`IMAGE_ROOTFS_ALIGNMENT` is added to the result
from the fourth step and "1" is subtracted.
In the sixth step, the remainder of the division between the result
from the fifth step and :term:`IMAGE_ROOTFS_ALIGNMENT` is subtracted from the
result of the fifth step. In this way, the result from the fourth step is
rounded up to the nearest multiple of :term:`IMAGE_ROOTFS_ALIGNMENT`.

Thus, if the :term:`IMAGE_ROOTFS_MAXSIZE` is set, is compared with the result
of the above calculations and is independent of the final image type.
No default value is set for :term:`IMAGE_ROOTFS_MAXSIZE`.

It's a good idea to set this variable for images that need to fit on a limited
space (e.g. SD card, a fixed-size partition, ...).
