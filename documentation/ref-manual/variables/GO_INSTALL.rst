When inheriting the :ref:`ref-classes-go` class, this optional variable
specifies which packages in the sources should be compiled and
installed in the Go build space by the
`go install <https://go.dev/ref/mod#go-install>`__ command.

Here is an example setting from the
:oe_git:`crucible </meta-openembedded/tree/meta-oe/recipes-support/crucible/>`
recipe::

   GO_INSTALL = "\
       ${GO_IMPORT}/cmd/crucible \
       ${GO_IMPORT}/cmd/habtool \
   "

By default, :term:`GO_INSTALL` is defined as::

   GO_INSTALL ?= "${GO_IMPORT}/..."

The ``...`` wildcard means that it will catch all
packages found in the sources.

See the :term:`GO_INSTALL_FILTEROUT` variable for
filtering out unwanted packages from the ones
found from the :term:`GO_INSTALL` value.
