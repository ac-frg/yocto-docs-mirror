See the BitBake manual for the initial description for this variable:
:term:`bitbake:SRC_URI`.

The following features are added by OpenEmbedded and the Yocto Project.

There are standard and recipe-specific options. Here are standard ones:

-  ``apply`` --- whether to apply the patch or not. The default
   action is to apply the patch.

-  ``striplevel`` --- which striplevel to use when applying the
   patch. The default level is 1.

-  ``patchdir`` --- specifies the directory in which the patch should
   be applied. The default is ``${``\ :term:`S`\ ``}``.

Here are options specific to recipes building code from a revision
control system:

-  ``mindate`` --- apply the patch only if
   :term:`SRCDATE` is equal to or greater than
   ``mindate``.

-  ``maxdate`` --- apply the patch only if :term:`SRCDATE` is not later
   than ``maxdate``.

-  ``minrev`` --- apply the patch only if :term:`SRCREV` is equal to or
   greater than ``minrev``.

-  ``maxrev`` --- apply the patch only if :term:`SRCREV` is not later
   than ``maxrev``.

-  ``rev`` --- apply the patch only if :term:`SRCREV` is equal to
   ``rev``.

-  ``notrev`` --- apply the patch only if :term:`SRCREV` is not equal to
   ``rev``.

.. note::

   If you want the build system to pick up files specified through
   a :term:`SRC_URI` statement from your append file, you need to be
   sure to extend the :term:`FILESPATH` variable by also using the
   :term:`FILESEXTRAPATHS` variable from within your append file.
