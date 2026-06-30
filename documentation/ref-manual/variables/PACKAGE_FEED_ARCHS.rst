Optionally specifies the package architectures used as part of the
package feed URIs during the build. When used, the
:term:`PACKAGE_FEED_ARCHS` variable is appended to the final package feed
URI, which is constructed using the
:term:`PACKAGE_FEED_URIS` and
:term:`PACKAGE_FEED_BASE_PATHS`
variables.

.. note::

   You can use the :term:`PACKAGE_FEED_ARCHS`
   variable to allow specific package architectures. If you do
   not need to allow specific architectures, which is a common
   case, you can omit this variable. Omitting the variable results in
   all available architectures for the current machine being included
   into remote package feeds.

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
