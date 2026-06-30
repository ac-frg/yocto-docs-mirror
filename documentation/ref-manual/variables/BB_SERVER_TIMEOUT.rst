Specifies the time (in seconds) after which to unload the BitBake
server due to inactivity. Set :term:`BB_SERVER_TIMEOUT` to determine how
long the BitBake server stays resident between invocations.

For example, the following statement in your ``local.conf`` file
instructs the server to be unloaded after 20 seconds of inactivity::

   BB_SERVER_TIMEOUT = "20"

If you want the server to never be unloaded,
set :term:`BB_SERVER_TIMEOUT` to "-1".
