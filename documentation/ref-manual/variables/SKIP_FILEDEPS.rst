Enables removal of all files from the "Provides" section of an RPM
package. Removal of these files is required for packages containing
prebuilt binaries and libraries such as ``libstdc++`` and ``glibc``.

To enable file removal, set the variable to "1" in your
``conf/local.conf`` configuration file in your:
:term:`Build Directory`::

   SKIP_FILEDEPS = "1"
