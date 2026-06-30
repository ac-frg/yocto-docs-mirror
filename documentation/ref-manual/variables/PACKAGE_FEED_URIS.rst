Specifies the front portion of the package feed URI used by the
OpenEmbedded build system. Each final package feed URI is comprised
of :term:`PACKAGE_FEED_URIS`,
:term:`PACKAGE_FEED_BASE_PATHS`, and
:term:`PACKAGE_FEED_ARCHS` variables.

Consider the following example where the :term:`PACKAGE_FEED_URIS`,
:term:`PACKAGE_FEED_BASE_PATHS`, and :term:`PACKAGE_FEED_ARCHS` variables are
defined in your ``local.conf`` file::

   PACKAGE_FEED_URIS = "https://example.com/packagerepos/release \
                        https://example.com/packagerepos/updates"
   PACKAGE_FEED_BASE_PATHS = "rpm rpm-dev"
   PACKAGE_FEED_ARCHS = "all core2-64"

Given these settings, the resulting package feeds are as follows:

.. code-block:: none

   https://example.com/packagerepos/release/rpm/all
   https://example.com/packagerepos/release/rpm/core2-64
   https://example.com/packagerepos/release/rpm-dev/all
   https://example.com/packagerepos/release/rpm-dev/core2-64
   https://example.com/packagerepos/updates/rpm/all
   https://example.com/packagerepos/updates/rpm/core2-64
   https://example.com/packagerepos/updates/rpm-dev/all
   https://example.com/packagerepos/updates/rpm-dev/core2-64
