Specifies the target controller to use when running tests against a
test image. The default controller to use is "qemu"::

   TEST_TARGET = "qemu"

A target controller is a class that defines how an image gets
deployed on a target and how a target is started. A layer can extend
the controllers by adding a module in the layer's
``/lib/oeqa/controllers`` directory and by inheriting the
``BaseTarget`` class, which is an abstract class that cannot be used
as a value of :term:`TEST_TARGET`.

You can provide the following arguments with :term:`TEST_TARGET`:

-  *"qemu":* Boots a QEMU image and runs the tests. See the
   ":ref:`test-manual/runtime-testing:enabling runtime tests on qemu`" section
   in the Yocto Project Test Environment Manual for more
   information.

-  *"simpleremote":* Runs the tests on target hardware that is
   already up and running. The hardware can be on the network or it
   can be a device running an image on QEMU. You must also set
   :term:`TEST_TARGET_IP` when you use
   "simpleremote".

   .. note::

      This argument is defined in
      ``meta/lib/oeqa/controllers/simpleremote.py``.

For information on running tests on hardware, see the
":ref:`test-manual/runtime-testing:enabling runtime tests on hardware`"
section in the Yocto Project Test Environment Manual.
