When inheriting the :ref:`ref-classes-kernel-yocto` class and when the
:term:`KMETA_AUDIT` variable is set to a non-empty string, the
:term:`KCONF_BSP_AUDIT_LEVEL` variable can be set to report:

#.  User-specified Kernel configurations that did not make it into the final
    Kernel configuration.

#.  Configurations defined in multiple input files with differing values.

Its value is a positive integer (default: 0):

-  0: no reporting is done.

-  1: reporting of configuration options that did not make it in the
   final configuration is done and is not limited to the current
   architecture (``ARCH``) in use.

-  2: reporting of configuration options that did not make it in the
   final configuration is done and is strictly limited to the current
   architecture (``ARCH``) in use.

-  3: report the problems found when this variable equals 2, and also
   report configurations options defined in multiple input files with
   differing values.

For value 1, 2 and 3 an error is produced if :term:`KMETA_AUDIT_WERROR`
is set.

For more details see the :ref:`ref-classes-kernel-yocto` class and the
:yocto_git:`symbol_why.py </yocto-kernel-tools/tree/tools/symbol_why.py>`
script in :yocto_git:`yocto-kernel-tools </yocto-kernel-tools>`.
