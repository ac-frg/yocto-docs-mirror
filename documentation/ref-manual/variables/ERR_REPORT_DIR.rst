When used with the :ref:`ref-classes-report-error` class, specifies the
path used for storing the debug files created by the :ref:`error reporting
tool <dev-manual/error-reporting-tool:using the error reporting tool>`,
which allows you to submit build errors you encounter to a central
database. By default, the value of this variable is
``${``\ :term:`LOG_DIR`\ ``}/error-report``.

You can set :term:`ERR_REPORT_DIR` to the path you want the error
reporting tool to store the debug files as follows in your
``local.conf`` file::

   ERR_REPORT_DIR = "path"
