Prevents BitBake from processing recipes and recipe append files.

You can use the :term:`BBMASK` variable to "hide" these ``.bb`` and
``.bbappend`` files. BitBake ignores any recipe or recipe append
files that match any of the expressions. It is as if BitBake does not
see them at all. Consequently, matching files are not parsed or
otherwise used by BitBake.

The values you provide are passed to Python's regular expression
compiler. Consequently, the syntax follows Python's Regular
Expression (re) syntax. The expressions are compared against the full
paths to the files. For complete syntax information, see Python's
documentation at https://docs.python.org/3/library/re.html#regular-expression-syntax.

The following example uses a complete regular expression to tell
BitBake to ignore all recipe and recipe append files in the
``meta-ti/recipes-misc/`` directory::

   BBMASK = "meta-ti/recipes-misc/"

If you want to mask out multiple directories or recipes, you can
specify multiple regular expression fragments. This next example
masks out multiple directories and individual recipes::

   BBMASK += "/meta-ti/recipes-misc/ meta-ti/recipes-ti/packagegroup/"
   BBMASK += "/meta-oe/recipes-support/"
   BBMASK += "/meta-foo/.*/openldap"
   BBMASK += "opencv.*\.bbappend"
   BBMASK += "lzma"

.. note::

   When specifying a directory name, use the trailing slash character
   to ensure you match just that directory name.
