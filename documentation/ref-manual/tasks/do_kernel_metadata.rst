Collects all the features required for a given kernel build, whether the
features come from :term:`SRC_URI` or from Git
repositories. After collection, the :term:`do_kernel_metadata` task
processes the features into a series of config fragments and patches,
which can then be applied by subsequent tasks such as
:term:`do_patch` and
:term:`do_kernel_configme`.
