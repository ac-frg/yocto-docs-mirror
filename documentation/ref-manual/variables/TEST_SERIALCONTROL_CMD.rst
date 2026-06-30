For automated hardware testing, specifies the command to use to
connect to the serial console of the target machine under test. This
command simply needs to connect to the serial console and forward
that connection to standard input and output as any normal terminal
program does.

For example, to use the Picocom terminal program on serial device
``/dev/ttyUSB0`` at 115200bps, you would set the variable as follows::

   TEST_SERIALCONTROL_CMD = "picocom /dev/ttyUSB0 -b 115200"
