Avoids QA errors when you use a non-common, non-CLOSED license in a
recipe. There are packages, such as the linux-firmware package, with many
licenses that are not in any way common. Also, new licenses are added
occasionally to avoid introducing a lot of common license files,
which are only applicable to a specific package.
:term:`NO_GENERIC_LICENSE` is used to allow copying a license that does
not exist in common licenses.

The following example shows how to add :term:`NO_GENERIC_LICENSE` to a
recipe::

   NO_GENERIC_LICENSE[license_name] = "license_file_in_fetched_source"

Here is an example that
uses the ``LICENSE.Abilis.txt`` file as the license from the fetched
source::

   NO_GENERIC_LICENSE[Firmware-Abilis] = "LICENSE.Abilis.txt"
