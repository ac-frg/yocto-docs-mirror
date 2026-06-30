Specifies the debug level of task signature check. 3 levels are supported:

* ``info``: displays a "Note" message to remind the user that a task is locked
  and the current signature matches the locked one.
* ``warn``: displays a "Warning" message if a task is locked and the current
  signature does not match the locked one.
* ``error``: same as warn but displays an "Error" message and aborts.
