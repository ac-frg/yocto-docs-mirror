Points to the base URL of the server and location within the
document-root that provides the metadata and packages required by
OPKG to support runtime package management of IPK packages. You set
this variable in your ``local.conf`` file.

Consider the following example::

   FEED_DEPLOYDIR_BASE_URI = "http://192.168.7.1/BOARD-dir"

This example assumes you are serving
your packages over HTTP and your databases are located in a directory
named ``BOARD-dir``, which is underneath your HTTP server's
document-root. In this case, the OpenEmbedded build system generates
a set of configuration files for you in your target that work with
the feed.
