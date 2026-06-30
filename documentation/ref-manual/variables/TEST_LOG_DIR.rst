Holds the SSH log and the boot log for QEMU machines. The
:term:`TEST_LOG_DIR` variable defaults to ``"${WORKDIR}/testimage"``.

.. note::

   Actual test results reside in the task log (``log.do_testimage``),
   which is in the ``${WORKDIR}/temp/`` directory.
