The number of leading dot-separated components of :term:`PV` that
constitute the stable version prefix. Used by the
:ref:`ref-classes-upstream-stable-release-point` class to generate
:term:`UPSTREAM_STABLE_RELEASE_REGEX`. Defaults to ``"2"``.

For example, with ``PV = "259.5"`` and ``STABLE_VERSION_PARTS = "1"``,
the generated regex matches versions starting with ``259``.
