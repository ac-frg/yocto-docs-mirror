If there are multiple versions of a recipe available, this variable
determines which version should be given preference. You must always
suffix the variable with the :term:`PN` you want to select (`python` in
the first example below), and you should specify the :term:`PV`
accordingly (`3.4.0` in the example).

The :term:`PREFERRED_VERSION` variable supports limited wildcard use
through the "``%``" character. You can use the character to match any
number of characters, which can be useful when specifying versions
that contain long revision numbers that potentially change. Here are
two examples::

   PREFERRED_VERSION_python = "3.4.0"
   PREFERRED_VERSION_linux-yocto = "5.0%"

.. note::

   The use of the "%" character is limited in that it only works at the end of the
   string. You cannot use the wildcard character in any other
   location of the string.

The specified version is matched against :term:`PV`, which does not
necessarily match the version part of the recipe's filename.

If you want to select a recipe named ``foo_git.bb`` which has :term:`PV`
set to ``1.2.3+git``, you can do so by setting ```PREFERRED_VERSION_foo``
to ``1.2.3%`` (i.e. simply setting ``PREFERRED_VERSION_foo`` to ``git``
will not work as the name of the recipe isn't used, but rather its
:term:`PV` definition).

Sometimes the :term:`PREFERRED_VERSION` variable can be set by
configuration files in a way that is hard to change. You can use
:term:`OVERRIDES` to set a machine-specific
override. Here is an example::

   PREFERRED_VERSION_linux-yocto:qemux86 = "5.0%"

Although not recommended, worst case, you can also use the
"forcevariable" override, which is the strongest override possible.
Here is an example::

   PREFERRED_VERSION_linux-yocto:forcevariable = "5.0%"

.. note::

   The ``:forcevariable`` override is not handled specially. This override
   only works because the default value of :term:`OVERRIDES` includes "forcevariable".

If a recipe with the specified version is not available, a warning
message will be shown. See :term:`REQUIRED_VERSION` if you want this
to be an error instead.
