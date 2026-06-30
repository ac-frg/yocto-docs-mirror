An ordered list of tests (modules) to run against an image when
performing automated runtime testing.

The OpenEmbedded build system provides a core set of tests that can
be used against images.

.. note::

   Currently, there is only support for running these tests under
   QEMU.

Tests include ``ping``, ``ssh``, ``df`` among others. You can add
your own tests to the list of tests by appending :term:`TEST_SUITES` as
follows::

   TEST_SUITES:append = " mytest"

Alternatively, you can
provide the "auto" option to have all applicable tests run against
the image::

   TEST_SUITES:append = " auto"

Using this option causes the
build system to automatically run tests that are applicable to the
image. Tests that are not applicable are skipped.

The order in which tests are run is important. Tests that depend on
another test must appear later in the list than the test on which
they depend. For example, if you append the list of tests with two
tests (``test_A`` and ``test_B``) where ``test_B`` is dependent on
``test_A``, then you must order the tests as follows::

   TEST_SUITES = "test_A test_B"

For more information on testing images, see the
":ref:`test-manual/runtime-testing:performing automated runtime testing`"
section in the Yocto Project Test Environment Manual.
