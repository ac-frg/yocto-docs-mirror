A list of shared state tasks added to the extensible SDK. By default,
the following tasks are added:

- :term:`do_populate_lic`
- :term:`do_package_qa`
- :term:`do_populate_sysroot`
- :term:`do_deploy`

Despite the default value of "" for the
:term:`SDK_RECRDEP_TASKS` variable, the above four tasks are always added
to the SDK. To specify tasks beyond these four, you need to use the
:term:`SDK_RECRDEP_TASKS` variable (e.g. you are defining additional
tasks that are needed in order to build
:term:`SDK_TARGETS`).
