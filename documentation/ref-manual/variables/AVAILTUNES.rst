The list of defined CPU and Application Binary Interface (ABI)
tunings (i.e. "tunes") available for use by the OpenEmbedded build
system.

The list simply presents the tunes that are available. Not all tunes
may be compatible with a particular machine configuration, or with
each other in a
:ref:`Multilib <dev-manual/libraries:combining multiple versions of library files into one image>`
configuration.

To add a tune to the list, be sure to append it with spaces using the
"+=" BitBake operator. Do not simply replace the list by using the
"=" operator. See the
":ref:`bitbake-user-manual/bitbake-user-manual-metadata:basic syntax`" section in the BitBake
User Manual for more information.
