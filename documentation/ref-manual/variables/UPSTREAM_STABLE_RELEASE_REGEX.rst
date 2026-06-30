A regular expression used to filter upstream versions during version
checks so that only versions within the same stable series are
considered. When set, BitBake's fetchers (git, wget, crate) apply this
regex to discovered upstream versions and discard any that do not match.

For example, if a recipe is at version ``1.4.2`` and the regex is
``^1\.4(\.\d+)*$``, then ``1.4.7`` would be a valid upgrade candidate
but ``1.5.0`` would not.

For recipes with dot-separated versions, inherit the
:ref:`ref-classes-upstream-stable-release-point` class to generate this
variable automatically. For other versioning schemes, set it directly::

   UPSTREAM_STABLE_RELEASE_REGEX = "^10\.2p\d+$"

See :ref:`ref-manual/release-process:stable point release upgrades` for
the criteria under which this variable should be set.
