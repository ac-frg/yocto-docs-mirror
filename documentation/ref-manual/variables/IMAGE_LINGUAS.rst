Specifies the list of locales to install into the image during the
root filesystem construction process. The OpenEmbedded build system
automatically splits locale files, which are used for localization,
into separate packages. Setting the :term:`IMAGE_LINGUAS` variable
ensures that any locale packages that correspond to packages already
selected for installation into the image are also installed. Here is
an example::

   IMAGE_LINGUAS = "pt-br de-de"

In this example, the build system ensures any Brazilian Portuguese
and German locale files that correspond to packages in the image are
installed (i.e. ``*-locale-pt-br`` and ``*-locale-de-de`` as well as
``*-locale-pt`` and ``*-locale-de``, since some software packages
only provide locale files by language and not by country-specific
language).

See the :term:`GLIBC_GENERATE_LOCALES`
variable for information on generating GLIBC locales.
