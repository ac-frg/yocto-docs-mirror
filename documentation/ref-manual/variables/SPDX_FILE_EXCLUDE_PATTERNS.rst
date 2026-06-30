A space-separated list of Python regular expressions used to exclude files
from the SPDX output when :term:`SPDX_INCLUDE_SOURCES` is enabled.
Files whose paths match any of the patterns, via ``re.search()``, are
filtered out from the generated SBOM.

By default this variable is empty, meaning no files are excluded.

Example usage::

   SPDX_FILE_EXCLUDE_PATTERNS = "\\.patch$ \\.diff$ /test/ \\.pyc$ \\.o$"

See also :term:`SPDX_INCLUDE_SOURCES`.
