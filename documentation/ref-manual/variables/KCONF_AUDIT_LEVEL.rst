When inheriting the :ref:`ref-classes-kernel-yocto` class and when the
:term:`KMETA_AUDIT` variable is set to a non-empty string, the
:term:`KCONF_AUDIT_LEVEL` variable specifies whether to report Kernel
configuration values that are different from the user-specified value. Its
value is a positive integer (default: 1):

-  0: no reporting is done.

-  1: report the problems as warnings and trigger an error if
   :term:`KMETA_AUDIT_WERROR` is set.

-  2: if the :term:`do_kernel_configme` has failed to generate a
   ``.config`` file, print the content of the ``merge_config_build.log``
   file containing the errors, instead of just providing the path to
   that file.

For more details see the :ref:`ref-classes-kernel-yocto` class and the
:yocto_git:`symbol_why.py </yocto-kernel-tools/tree/tools/symbol_why.py>`
script in :yocto_git:`yocto-kernel-tools </yocto-kernel-tools>`.
