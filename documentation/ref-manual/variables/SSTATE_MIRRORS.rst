Configures the OpenEmbedded build system to search other mirror
locations for prebuilt cache data objects before building out the
data. This variable works like fetcher :term:`MIRRORS`
and :term:`PREMIRRORS` and points to the cache
locations to check for the shared state (sstate) objects.

You can specify a filesystem directory or a remote URL such as HTTP
or FTP. The locations you specify need to contain the shared state
cache (sstate-cache) results from previous builds. The sstate-cache
you point to can also be from builds on other machines.

When pointing to sstate build artifacts on another machine that uses
a different GCC version for native builds, you must configure
:term:`SSTATE_MIRRORS` with a regular expression that maps local search
paths to server paths. The paths need to take into account
:term:`NATIVELSBSTRING` set by the :ref:`ref-classes-uninative` class.
For example, the following maps the local search path ``universal-4.9``
to the server-provided path server_url_sstate_path::

   SSTATE_MIRRORS ?= "file://universal-4.9/(.*) https://server_url_sstate_path/universal-4.8/\1"

If a mirror uses the same structure as
:term:`SSTATE_DIR`, you need to add "PATH" at the
end as shown in the examples below. The build system substitutes the
correct path within the directory structure::

   SSTATE_MIRRORS ?= "\
       file://.* https://someserver.tld/share/sstate/PATH;downloadfilename=PATH \
       file://.* file:///some-local-dir/sstate/PATH"

.. note::

   If the mirror is protected behind a username and password, the
   :term:`build host` needs to be configured so the :term:`build system
   <OpenEmbedded Build System>` is able to download the sstate cache using
   authentication.

   The recommended way to do that is by setting the following parameters
   in ``$HOME/.netrc`` (``$HOME`` being the :term:`build host` home
   directory)::

      machine someserver.tld
      login <user>
      password <password>

   This file requires permissions set to ``400`` or ``600`` to prevent
   other users from reading the file::

      chmod 600 "$HOME/.netrc"

   Another method to configure the username and password is from the
   URL in :term:`SSTATE_MIRRORS` directly, with the ``user`` and ``pswd``
   parameters::

      SSTATE_MIRRORS ?= "\
          file://.* https://someserver.tld/share/sstate/PATH;user=<user>;pswd=<password>;downloadfilename=PATH \
      "

The Yocto Project actually shares the cache data objects built by its
autobuilder::

   SSTATE_MIRRORS ?= "file://.* http://sstate.yoctoproject.org/all/PATH;downloadfilename=PATH"

As such binary artifacts are built for the generic QEMU machines
supported by the various Poky releases, they are less likely to be
reusable in real projects building binaries optimized for a specific
CPU family.
