This variable is used for storing image conversion commands.
Image conversion can convert an image into different objects like:

-   Compressed version of the image

-   Checksums for the image

An example of :term:`CONVERSION_CMD` from :ref:`ref-classes-image_types`
class is::

   CONVERSION_CMD:lzo = "lzop -9 ${IMAGE_NAME}${IMAGE_NAME_SUFFIX}.${type}"
