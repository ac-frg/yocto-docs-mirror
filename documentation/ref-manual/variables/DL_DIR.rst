The central download directory used by the build process to store
downloads. By default, :term:`DL_DIR` gets files suitable for mirroring
for everything except Git repositories. If you want tarballs of Git
repositories, use the
:term:`BB_GENERATE_MIRROR_TARBALLS`
variable.

You can set this directory by defining the :term:`DL_DIR` variable in the
``conf/local.conf`` file. This directory is self-maintaining and you
should not have to touch it. By default, the directory is
``downloads`` in the :term:`Build Directory`::

   #DL_DIR ?= "${TOPDIR}/downloads"

To specify a different download directory,
simply remove the comment from the line and provide your directory.

During a first build, the system downloads many different source code
tarballs from various upstream projects. Downloading can take a
while, particularly if your network connection is slow. Tarballs are
all stored in the directory defined by :term:`DL_DIR` and the build
system looks there first to find source tarballs.

.. note::

   When wiping and rebuilding, you can preserve this directory to
   speed up this part of subsequent builds.

You can safely share this directory between multiple builds on the
same development machine. For additional information on how the build
process gets source files when working behind a firewall or proxy
server, see this specific question in the ":doc:`/ref-manual/faq`"
chapter. You can also refer to the
":yocto_wiki:`Working Behind a Network Proxy </Working_Behind_a_Network_Proxy>`"
Wiki page.
