Specifies a space-separated list of license names (as they would
appear in :term:`LICENSE`) that should be excluded
from the build (if set globally), or from an image (if set locally
in an image recipe).

When the variable is set globally, recipes that provide no alternatives to listed
incompatible licenses are not built. Packages that are individually
licensed with the specified incompatible licenses will be deleted.
Most of the time this does not allow a feasible build (because it becomes impossible
to satisfy build time dependencies), so the recommended way to
implement license restrictions is to set the variable in specific
image recipes where the restrictions must apply. That way there
are no build time restrictions, but the license check is still
performed when the image's filesystem is assembled from packages.

There is some support for wildcards in this variable's value,
however it is restricted to specific licenses. Currently only
these wildcards are allowed and expand as follows:

- ``AGPL-3.0*"``: ``AGPL-3.0-only``, ``AGPL-3.0-or-later``
- ``GPL-3.0*``: ``GPL-3.0-only``, ``GPL-3.0-or-later``
- ``LGPL-3.0*``: ``LGPL-3.0-only``, ``LGPL-3.0-or-later``

.. note::

   This functionality is only regularly tested using the following
   setting::

           INCOMPATIBLE_LICENSE = "GPL-3.0* LGPL-3.0* AGPL-3.0*"


   Although you can use other settings, you might be required to
   remove dependencies on (or provide alternatives to) components that
   are required to produce a functional system image.
