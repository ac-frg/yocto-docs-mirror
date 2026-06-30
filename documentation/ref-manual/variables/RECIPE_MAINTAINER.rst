This variable defines the name and e-mail address of the maintainer of a
recipe. Such information can be used by human users submitted changes,
and by automated tools to send notifications, for example about
vulnerabilities or source updates.

The variable can be defined in a global distribution :oe_git:`maintainers.inc
</openembedded-core/tree/meta/conf/distro/include/maintainers.inc>` file::

    meta/conf/distro/include/maintainers.inc:RECIPE_MAINTAINER:pn-sysvinit = "Ross Burton <ross.burton@arm.com>"

It can also be directly defined in a recipe,
for example in the ``libgpiod`` one::

    RECIPE_MAINTAINER = "Bartosz Golaszewski <brgl@bgdev.pl>"
