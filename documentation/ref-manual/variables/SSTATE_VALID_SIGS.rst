When verifying :ref:`shared state <overview-manual/concepts:setscene tasks
and shared state>` artifacts (when :term:`SSTATE_VERIFY_SIG` is set to
"1"), the :term:`SSTATE_VALID_SIGS` variable is a space-separated list of
:wikipedia:`GPG <GNU_Privacy_Guard>` key identifiers to use to verify their
signature.

It must contain the short form identifier of the key pair. For example,
when running the ``gpg --list-keys`` command (in bold text below):

.. parsed-literal::

   pub   ed25519 2026-04-17 [SC]
         \4049A47E3AAA99D0250966DC\ **5B97632FA7F4E942**
   uid           [ultimate] Antonin Godard (SState Signing) <antonin.godard\@bootlin.com>
   sub   cv25519 2026-04-17 [E]

The short form equals the last 16 characters of the identifier. In the
above example: ``5B97632FA7F4E942``.

.. note::

   If this variable is empty (the default), any of the GPG key present on
   the :term:`Build Host` can be used by the :term:`OpenEmbedded Build
   System` to verify the shared state artifacts.

See :doc:`/security-manual/sstate-signing` in the Yocto Project Security
Manual for more information.
