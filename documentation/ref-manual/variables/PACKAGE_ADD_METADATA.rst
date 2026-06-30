This variable defines additional metadata to add to packages.

You may find you need to inject additional metadata into packages.
This variable allows you to do that by setting the injected data as
the value. Multiple fields can be added by splitting the content with
the literal separator "\n".

The suffixes '_IPK', '_DEB', or '_RPM' can be applied to the variable
to do package type specific settings. It can also be made package
specific by using the package name as a suffix.

You can find out more about applying this variable in the
":ref:`dev-manual/packages:adding custom metadata to packages`"
section in the Yocto Project Development Tasks Manual.
