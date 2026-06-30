Specifies the directory used by the build system to find templates
from which to build the ``bblayers.conf`` and ``local.conf`` files.
Use this variable if you wish to customize such files, and the default
BitBake targets shown when sourcing the ``oe-init-build-env`` script.

For details, see the
:ref:`dev-manual/custom-template-configuration-directory:creating a custom template configuration directory`
section in the Yocto Project Development Tasks manual.

.. note::

   You must set this variable in the external environment in order
   for it to work.
