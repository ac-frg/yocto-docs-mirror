Adds details about a flag in :term:`LICENSE_FLAGS`. This way,
if such a flag is not accepted through :term:`LICENSE_FLAGS_ACCEPTED`,
the error message will be more informative, containing the specified
extra details.

For example, a recipe with an EULA may set::

   LICENSE_FLAGS = "FooBar-EULA"
   LICENSE_FLAGS_DETAILS[FooBar-EULA] = "For further details, see https://example.com/eula."

If ``Foobar-EULA`` isn't in :term:`LICENSE_FLAGS_ACCEPTED`, the
error message is more useful::

  Has a restricted license 'FooBar-EULA' which is not listed in your LICENSE_FLAGS_ACCEPTED.
  For further details, see https://example.com/eula.
