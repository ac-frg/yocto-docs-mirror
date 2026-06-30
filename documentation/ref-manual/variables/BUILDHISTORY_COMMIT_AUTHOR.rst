When inheriting the :ref:`ref-classes-buildhistory`
class, this variable specifies the author to use for each Git commit.
In order for the :term:`BUILDHISTORY_COMMIT_AUTHOR` variable to work, the
:term:`BUILDHISTORY_COMMIT` variable must
be set to "1".

Git requires that the value you provide for the
:term:`BUILDHISTORY_COMMIT_AUTHOR` variable takes the form of "name
email@host". Providing an email address or host that is not valid
does not produce an error.

By default, the :ref:`ref-classes-buildhistory` class sets the variable
as follows::

   BUILDHISTORY_COMMIT_AUTHOR ?= "buildhistory <buildhistory@${DISTRO}>"
