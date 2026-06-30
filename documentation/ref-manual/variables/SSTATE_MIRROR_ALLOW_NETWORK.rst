If set to "1", allows fetches from mirrors that are specified in
:term:`SSTATE_MIRRORS` to work even when
fetching from the network is disabled by setting :term:`BB_NO_NETWORK` to
"1". Using the :term:`SSTATE_MIRROR_ALLOW_NETWORK` variable is useful if
you have set :term:`SSTATE_MIRRORS` to point to an internal server for
your shared state cache, but you want to disable any other fetching
from the network.
