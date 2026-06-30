Specifies the path to the directory containing binary configuration
scripts. These scripts provide configuration information for other
software that wants to make use of libraries or include files
provided by the software associated with the script.

.. note::

   This style of build configuration has been largely replaced by
   ``pkg-config``. Consequently, if ``pkg-config`` is supported by the
   library to which you are linking, it is recommended you use
   ``pkg-config`` instead of a provided configuration script.
