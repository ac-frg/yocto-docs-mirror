If there are many CVEs with the same status and reason, they can by simplified by using this
variable instead of many similar lines with :term:`CVE_STATUS`::

   CVE_STATUS_GROUPS = "CVE_STATUS_WIN CVE_STATUS_PATCHED"

   CVE_STATUS_WIN = "CVE-1234-0001 CVE-1234-0002"
   CVE_STATUS_WIN[status] = "not-applicable-platform: Issue only applies on Windows"
   CVE_STATUS_PATCHED = "CVE-1234-0003 CVE-1234-0004"
   CVE_STATUS_PATCHED[status] = "fixed-version: Fixed externally"
