A list of recipes that should not be built for multilib. OE-Core's
``multilib.conf`` file defines a reasonable starting point for this
list with::

   NON_MULTILIB_RECIPES = "grub grub-efi make-mod-scripts ovmf u-boot"
