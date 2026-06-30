When inheriting the :ref:`ref-classes-go` class, this mandatory variable
sets the import path for the Go package that will be created for the code
to build. If you have a ``go.mod`` file in the source directory, this
typically matches the path in the ``module`` line in this file.

Other Go programs importing this package will use this path.

Here is an example setting from the
:oe_git:`go-helloworld_0.1.bb </openembedded-core/tree/meta/recipes-extended/go-examples/go-helloworld_0.1.bb>`
recipe::

    GO_IMPORT = "golang.org/x/example"
