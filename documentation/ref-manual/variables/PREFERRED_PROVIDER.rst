If multiple recipes provide the same item, this variable determines
which recipe is preferred and thus provides the item (i.e. the
preferred provider). You should always suffix this variable with the
name of the provided item. And, you should define the variable using
the preferred recipe's name (:term:`PN`). Here is a common
example::

   PREFERRED_PROVIDER_virtual/kernel ?= "linux-yocto"

In the previous example, multiple recipes are providing "virtual/kernel".
The :term:`PREFERRED_PROVIDER` variable is set with the name (:term:`PN`) of
the recipe you prefer to provide "virtual/kernel".

Here are more examples::

   PREFERRED_PROVIDER_virtual/xserver = "xserver-xf86"
   PREFERRED_PROVIDER_virtual/libgl ?= "mesa"

For more
information, see the ":ref:`dev-manual/new-recipe:using virtual providers`"
section in the Yocto Project Development Tasks Manual.

.. note::

   If you use a ``virtual/\*`` item with :term:`PREFERRED_PROVIDER`, then any
   recipe that :term:`PROVIDES` that item but is not selected (defined)
   by :term:`PREFERRED_PROVIDER` is prevented from building, which is usually
   desirable since this mechanism is designed to select between mutually
   exclusive alternative providers.
