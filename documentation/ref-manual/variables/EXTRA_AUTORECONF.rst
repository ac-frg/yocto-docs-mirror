For recipes inheriting the :ref:`ref-classes-autotools`
class, you can use :term:`EXTRA_AUTORECONF` to specify extra options to
pass to the ``autoreconf`` command that is executed during the
:term:`do_configure` task.

The default value is "--exclude=autopoint".
