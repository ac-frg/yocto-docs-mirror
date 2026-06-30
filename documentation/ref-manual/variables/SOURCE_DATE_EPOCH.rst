This defines a date expressed in number of seconds since
the UNIX EPOCH (01 Jan 1970 00:00:00 UTC), which is used by
multiple build systems to force a timestamp in built binaries.
Many upstream projects already support this variable.

You will find more details in the `official specifications
<https://reproducible-builds.org/specs/source-date-epoch/>`__.

A value for each recipe is computed from the sources by
:oe_git:`meta/lib/oe/reproducible.py </openembedded-core/tree/meta/lib/oe/reproducible.py>`.

If a recipe wishes to override the default behavior, it should set its
own :term:`SOURCE_DATE_EPOCH` value::

    SOURCE_DATE_EPOCH = "1613559011"
