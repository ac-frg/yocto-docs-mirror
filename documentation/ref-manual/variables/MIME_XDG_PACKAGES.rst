The current implementation of the :ref:`ref-classes-mime-xdg`
class cannot detect ``.desktop`` files installed through absolute
symbolic links. Use this setting to make the class create post-install
and post-remove scripts for these packages anyway, to invoke the
``update-destop-database`` command.
