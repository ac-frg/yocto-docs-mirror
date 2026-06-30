Defines a serial console (TTY) to enable using
:wikipedia:`getty <Getty_(Unix)>`. Provide a value that specifies the
baud rate followed by the TTY device name separated by a semicolon.
Use spaces to separate multiple devices::

   SERIAL_CONSOLES = "115200;ttyS0 115200;ttyS1"
