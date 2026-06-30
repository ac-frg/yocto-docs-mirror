Specifies a list of options that, if reported by the configure script
as being invalid, should not generate a warning during the
:term:`do_configure` task. Normally, invalid
configure options are simply not passed to the configure script (e.g.
should be removed from :term:`EXTRA_OECONF` or
:term:`PACKAGECONFIG_CONFARGS`).
However, there are common options that are passed to all
configure scripts at a class level, but might not be valid for some
configure scripts. Therefore warnings about these options are useless.
For these cases, the options are added to :term:`UNKNOWN_CONFIGURE_OPT_IGNORE`.

The configure arguments check that uses
:term:`UNKNOWN_CONFIGURE_OPT_IGNORE` is part of the
:ref:`ref-classes-insane` class and is only enabled if the
recipe inherits the :ref:`ref-classes-autotools` class.
