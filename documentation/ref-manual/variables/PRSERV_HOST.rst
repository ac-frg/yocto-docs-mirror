The network based :term:`PR` service host and port.

The ``conf/templates/default/local.conf.sample.extended`` configuration
file in :yocto_git:`meta-poky </meta-yocto/tree/meta-poky>` shows how the
:term:`PRSERV_HOST` variable is set::

   PRSERV_HOST = "localhost:0"

You must
set the variable if you want to automatically start a local :ref:`PR
service <dev-manual/packages:working with a pr service>`. You can
set :term:`PRSERV_HOST` to other values to use a remote PR service.
