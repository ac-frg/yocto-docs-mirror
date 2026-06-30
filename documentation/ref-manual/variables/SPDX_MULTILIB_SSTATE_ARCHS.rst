The list of sstate architectures to consider when collecting SPDX
dependencies. This includes multilib architectures when multilib is
enabled.

The default value is set to the value of ``SSTATE_ARCHS``.

This variable is used internally by the SPDX generation classes to
ensure all relevant dependencies are included in the SBOM,
regardless of whether multilib is enabled or not.
