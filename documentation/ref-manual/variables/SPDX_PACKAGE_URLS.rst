A space-separated list of Package URLs ("PURLs") for the software package.
The first item in this list will be listed as the ``packageUrl`` property
of the packages, and all PURLs (including the first one) will be listed as
external references. The default value is an auto-generated ``pkg:yocto``
PURL based on the recipe name, version, and layer name. Override this
variable to replace the default, otherwise append or prepend to add
additional PURLs.
