This is a required field in an OpenEmbedded recipe file, and should
contain a list of source licenses for the recipe. Follow these rules:

-  Do not use spaces within individual license names.

-  Separate license names using \| (pipe) when there is a choice
   between licenses.

-  Separate license names using & (ampersand) when there are
   multiple licenses for different parts of the source.

-  You can use spaces between license names.

-  For standard licenses, use the names of the files in
   ``meta/files/common-licenses/`` or the
   :term:`SPDXLICENSEMAP` flag names defined in
   ``meta/conf/licenses.conf``.

Here are some examples::

   LICENSE = "LGPL-2.1-only | GPL-3.0-only"
   LICENSE = "MPL-1.0 & LGPL-2.1-only"
   LICENSE = "GPL-2.0-or-later"

The first example is from the
recipes for Qt, which the user may choose to distribute under either
the LGPL version 2.1 or GPL version 3. The second example is from
Cairo where two licenses cover different parts of the source code.
The final example is from ``sysstat``, which presents a single
license.

You can also specify licenses on a per-package basis to handle
situations where components of the output have different licenses.
For example, a piece of software whose code is licensed under GPLv2
but has accompanying documentation licensed under the GNU Free
Documentation License 1.2 could be specified as follows::

   LICENSE = "GFDL-1.2 & GPL-2.0-only"
   LICENSE:${PN} = "GPL-2.0.only"
   LICENSE:${PN}-doc = "GFDL-1.2"

.. note::

   A recipe's :term:`LICENSE` value must be accompanied by an associated
   :term:`LIC_FILES_CHKSUM` value, except in the special case where
   the :term:`LICENSE` value is set to "CLOSED".
