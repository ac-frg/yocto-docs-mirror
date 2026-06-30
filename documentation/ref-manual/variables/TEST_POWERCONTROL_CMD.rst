For automated hardware testing, specifies the command to use to
control the power of the target machine under test. Typically, this
command would point to a script that performs the appropriate action
(e.g. interacting with a web-enabled power strip). The specified
command should expect to receive as the last argument "off", "on" or
"cycle" specifying to power off, on, or cycle (power off and then
power on) the device, respectively.
