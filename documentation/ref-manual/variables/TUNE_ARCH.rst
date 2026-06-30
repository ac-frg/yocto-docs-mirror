The GNU canonical architecture for a specific architecture (i.e.
``arm``, ``armeb``, ``mips``, ``mips64``, and so forth). BitBake uses
this value to setup configuration.

:term:`TUNE_ARCH` definitions are specific to a given architecture. The
definitions can be a single static definition, or can be dynamically
adjusted. You can see details for a given CPU family by looking at
the architecture's ``README`` file. For example, the
``meta/conf/machine/include/mips/README`` file in
:term:`OpenEmbedded-Core (OE-Core)` provides information for
:term:`TUNE_ARCH` specific to the ``mips`` architecture.

:term:`TUNE_ARCH` is tied closely to
:term:`TARGET_ARCH`, which defines the target
machine's architecture. The BitBake configuration file
(``meta/conf/bitbake.conf``) sets :term:`TARGET_ARCH` as follows::

   TARGET_ARCH = "${TUNE_ARCH}"

The following list, which is by no means complete since architectures
are configurable, shows supported machine architectures:

- arm
- i586
- x86_64
- powerpc
- powerpc64
- mips
- mipsel
