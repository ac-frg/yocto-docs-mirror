When using Go Modules, the current working directory must be the directory
containing the ``go.mod`` file, or one of its subdirectories. When the
``go`` tool is used, it will automatically look for the ``go.mod`` file
in the Go working directory or in any parent directory, but not in
subdirectories.

When using the :ref:`ref-classes-go-mod` class to use Go modules,
the optional :term:`GO_WORKDIR` variable, defaulting to the value
of :term:`GO_IMPORT`, allows to specify a different Go working directory.
