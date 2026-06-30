When set to "1", specifies to include the toolchain in the extensible
SDK. Including the toolchain is useful particularly when
:term:`SDK_EXT_TYPE` is set to "minimal" to keep
the SDK reasonably small but you still want to provide a usable
toolchain. For example, suppose you want to use the toolchain from an
IDE or from other tools and you do not want to perform additional
steps to install the toolchain.

The :term:`SDK_INCLUDE_TOOLCHAIN` variable defaults to "0" if
:term:`SDK_EXT_TYPE` is set to "minimal", and defaults to "1" if
:term:`SDK_EXT_TYPE` is set to "full".
