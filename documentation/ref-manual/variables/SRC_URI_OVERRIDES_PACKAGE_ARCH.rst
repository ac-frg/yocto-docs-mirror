By default, the OpenEmbedded build system automatically detects
whether :term:`SRC_URI` contains files that are machine-specific. If so,
the build system automatically changes :term:`PACKAGE_ARCH`. Setting this
variable to "0" disables this behavior.
