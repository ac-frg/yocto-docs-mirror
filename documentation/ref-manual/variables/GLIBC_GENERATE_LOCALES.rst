Specifies the list of GLIBC locales to generate should you not wish
to generate all LIBC locals, which can be time consuming.

.. note::

   If you specifically remove the locale ``en_US.UTF-8``, you must set
   :term:`IMAGE_LINGUAS` appropriately.

You can set :term:`GLIBC_GENERATE_LOCALES` in your ``local.conf`` file.
By default, all locales are generated::

   GLIBC_GENERATE_LOCALES = "en_GB.UTF-8 en_US.UTF-8"
