Specifies the optimization flags passed to the C compiler when
building for the target. The flags are passed through the default
value of the :term:`TARGET_CFLAGS` variable.

The :term:`SELECTED_OPTIMIZATION` variable takes the value of
:term:`FULL_OPTIMIZATION` unless :term:`DEBUG_BUILD` = "1", in which
case the value of :term:`DEBUG_OPTIMIZATION` is used.
