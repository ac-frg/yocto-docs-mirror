When inheriting the :ref:`ref-classes-buildhistory` class, this variable
optionally specifies a remote repository to which build history pushes
Git changes. In order for :term:`BUILDHISTORY_PUSH_REPO` to work,
:term:`BUILDHISTORY_COMMIT` must be set to "1".

The repository should correspond to a remote address that specifies a
repository as understood by Git, or alternatively to a remote name
that you have set up manually using ``git remote`` within the local
repository.

By default, the :ref:`ref-classes-buildhistory` class sets the variable
as follows::

   BUILDHISTORY_PUSH_REPO ?= ""
