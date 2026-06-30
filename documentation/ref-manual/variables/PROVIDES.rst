A list of aliases by which a particular recipe can be known. By
default, a recipe's own :term:`PN` is implicitly already in its
:term:`PROVIDES` list and therefore does not need to mention that it
provides itself. If a recipe uses :term:`PROVIDES`, the additional
aliases are synonyms for the recipe and can be useful for satisfying
dependencies of other recipes during the build as specified by
:term:`DEPENDS`.

Consider the following example :term:`PROVIDES` statement from the recipe
file ``eudev_3.2.9.bb``::

   PROVIDES += "udev"

The :term:`PROVIDES` statement
results in the "eudev" recipe also being available as simply "udev".

.. note::

   A recipe's own recipe name (:term:`PN`) is always implicitly prepended
   to :term:`PROVIDES`, so while using "+=" in the above example may not be
   strictly necessary it is recommended to avoid confusion.

In addition to providing recipes under alternate names, the
:term:`PROVIDES` mechanism is also used to implement virtual targets. A
virtual target is a name that corresponds to some particular
functionality (e.g. a Linux kernel). Recipes that provide the
functionality in question list the virtual target in :term:`PROVIDES`.
Recipes that depend on the functionality in question can include the
virtual target in :term:`DEPENDS` to leave the choice of provider open.

Conventionally, virtual targets have names on the form
"virtual/function" (e.g. "virtual/kernel"). The slash is simply part
of the name and has no syntactical significance.

The :term:`PREFERRED_PROVIDER` variable is
used to select which particular recipe provides a virtual target.

.. note::

   A corresponding mechanism for virtual runtime dependencies (packages)
   exists. However, the mechanism does not depend on any special
   functionality beyond ordinary variable assignments. For example,
   :term:`VIRTUAL-RUNTIME_dev_manager <VIRTUAL-RUNTIME>` refers to the
   package of the component that manages the ``/dev`` directory.

   Setting the "preferred provider" for runtime dependencies is as
   simple as using the following assignment in a configuration file::

           VIRTUAL-RUNTIME_dev_manager = "udev"
