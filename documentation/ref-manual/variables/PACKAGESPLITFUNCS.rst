Specifies a list of functions run to perform additional splitting of
files into individual packages. Recipes can either prepend to this
variable or prepend to the ``populate_packages`` function in order to
perform additional package splitting. In either case, the function
should set :term:`PACKAGES`,
:term:`FILES`, :term:`RDEPENDS` and
other packaging variables appropriately in order to perform the
desired splitting.
