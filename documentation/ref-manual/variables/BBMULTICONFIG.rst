Specifies each additional separate configuration when you are
building targets with multiple configurations. Use this variable in
your ``conf/local.conf`` configuration file. Specify a
multiconfigname for each configuration file you are using. For
example, the following line specifies three configuration files::

   BBMULTICONFIG = "configA configB configC"

Each configuration file you use must reside in a ``multiconfig``
subdirectory of a configuration directory within a layer, or
within the :term:`Build Directory` (e.g.
``build_directory/conf/multiconfig/configA.conf`` or
``mylayer/conf/multiconfig/configB.conf``).

For information on how to use :term:`BBMULTICONFIG` in an environment
that supports building targets with multiple configurations, see the
":ref:`dev-manual/building:building images for multiple targets using multiple configurations`"
section in the Yocto Project Development Tasks Manual.
