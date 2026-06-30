The CVE ID which is patched or should be ignored. Here is
an example from the :oe_layerindex:`Python3 recipe</layerindex/recipe/23823>`::

   CVE_STATUS[CVE-2020-15523] = "not-applicable-platform: Issue only applies on Windows"

It has the format "reason: description" and the description is optional.
The Reason is mapped to the final CVE state by mapping via
:term:`CVE_CHECK_STATUSMAP`. See :ref:`security-manual/vulnerabilities:fixing vulnerabilities in recipes`
for details.
