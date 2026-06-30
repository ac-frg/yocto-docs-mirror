Disables auto package from splitting ``.debug`` files. If a recipe
requires ``FILES:${PN}-dbg`` to be set manually, the
:term:`NOAUTOPACKAGEDEBUG` can be defined allowing you to define the
content of the debug package. For example::

   NOAUTOPACKAGEDEBUG = "1"
   FILES:${PN}-dev = "${includedir}/${QT_DIR_NAME}/Qt/*"
   FILES:${PN}-dbg = "/usr/src/debug/"
   FILES:${QT_BASE_NAME}-demos-doc = "${docdir}/${QT_DIR_NAME}/qch/qt.qch"
