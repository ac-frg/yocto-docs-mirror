If there are multiple versions of a recipe available, this variable
determines which version should be given preference.
:term:`REQUIRED_VERSION` works in exactly the same manner as
:term:`PREFERRED_VERSION`, except that if the specified version is not
available then an error message is shown and the build fails
immediately.

If both :term:`REQUIRED_VERSION` and :term:`PREFERRED_VERSION` are set
for the same recipe, the :term:`REQUIRED_VERSION` value applies.
