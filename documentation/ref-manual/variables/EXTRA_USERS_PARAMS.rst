When inheriting the :ref:`ref-classes-extrausers`
class, this variable provides image level user and group operations.
This is a more global method of providing user and group
configuration as compared to using the
:ref:`ref-classes-useradd` class, which ties user and
group configurations to a specific recipe.

The set list of commands you can configure using the
:term:`EXTRA_USERS_PARAMS` is shown in the
:ref:`ref-classes-extrausers` class. These commands map to the normal
Unix commands of the same names::

   # EXTRA_USERS_PARAMS = "\
   # useradd -p '' tester; \
   # groupadd developers; \
   # userdel nobody; \
   # groupdel -g video; \
   # groupmod -g 1020 developers; \
   # usermod -s /bin/sh tester; \
   # "

Hardcoded passwords are supported via the ``-p`` parameters for
``useradd`` or ``usermod``, but only hashed.

Here is an example that adds two users named "tester-jim" and "tester-sue" and assigns
passwords. First on host, create the (escaped) password hash::

   printf "%q" $(mkpasswd -m sha256crypt tester01)

The resulting hash is set to a variable and used in ``useradd`` command parameters::

   inherit extrausers
   PASSWD = "\$X\$ABC123\$A-Long-Hash"
   EXTRA_USERS_PARAMS = "\
       useradd -p '${PASSWD}' tester-jim; \
       useradd -p '${PASSWD}' tester-sue; \
       "

Finally, here is an example that sets the root password::

   inherit extrausers
   EXTRA_USERS_PARAMS = "\
       usermod -p '${PASSWD}' root; \
       "

.. note::

   From a security perspective, hardcoding a default password is not
   generally a good idea or even legal in some jurisdictions. It is
   recommended that you do not do this if you are building a production
   image.

Additionally there is a special ``passwd-expire`` command that will
cause the password for a user to be expired and thus force changing it
on first login, for example::

   EXTRA_USERS_PARAMS += " useradd myuser; passwd-expire myuser;"

.. note::

   At present, ``passwd-expire`` may only work for remote logins when
   using OpenSSH and not dropbear as an SSH server.
