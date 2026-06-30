In a recipe, defines the version used to match the recipe version
against the version in the `NIST CVE database <https://nvd.nist.gov/>`__
when using the :ref:`ref-classes-vex` or :ref:`ref-classes-create-spdx`
class.

The default is ${:term:`PV`} but if recipes use custom version numbers
which do not map to upstream software component release versions and the versions
used in the CVE database, then this variable can be used to set the
version number for :ref:`ref-classes-vex` or
:ref:`ref-classes-create-spdx`. Example::

    CVE_VERSION = "2.39"
