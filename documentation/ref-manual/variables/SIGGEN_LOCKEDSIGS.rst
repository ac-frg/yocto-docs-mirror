The list of locked tasks, with the form::

  SIGGEN_LOCKEDSIGS += "<package>:<task>:<signature>"

If ``<signature>`` exists for the specified ``<task>`` and ``<package>``
in the sstate cache, BitBake will use the cached output instead of
rebuilding the ``<task>``. If it does not exist, BitBake will build the
``<task>`` and the sstate cache will be used next time.

Example::

  SIGGEN_LOCKEDSIGS += "bc:do_compile:09772aa4532512baf96d433484f27234d4b7c11dd9cda0d6f56fa1b7ce6f25f0"

You can obtain the signature of all the tasks for the recipe ``bc`` using::

  bitbake -S none bc

Then you can look at files in ``build/tmp/stamps/<arch>/bc`` and look for
files like: ``<PV>.do_compile.sigdata.09772aa4532512baf96d433484f27234d4b7c11dd9cda0d6f56fa1b7ce6f25f0``.

Alternatively, you can also use :doc:`bblock </dev-manual/bblock>` to
generate this line for you.
