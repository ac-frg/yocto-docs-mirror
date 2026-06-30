Specifies the number of parallel threads that should be used when
using xz compression.

By default this scales with core count, but is never set less than 2
to ensure that multi-threaded mode is always used so that the output
file contents are deterministic. Builds will work with a value of 1
but the output will differ compared to the output from the compression
generated when more than one thread is used.

On systems where many tasks run in parallel, setting a limit to this
can be helpful in controlling system resource usage.
