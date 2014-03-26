============================
GNU MediaGoblin init scripts
============================

.. image:: http://api.flattr.com/button/flattr-badge-large.png
    :target: http://flattr.com/thing/695398/jwandborgmediagoblin-init-scripts-on-GitHub

Run your MediaGoblin server and task queue as services that start
automatically on reboot.

These scripts should free you of some burdens, and if you don't feel you
have any, you might not need them :)

Compatibility
-------------

These MediaGoblin init scripts are compatible with `Debian's
dependency-based boot sequence`_. They use functions sourced from
``/lib/lsb/init-functions`` and are installed with ``insserv``.

.. _`Debian's dependency-based boot sequence`: http://wiki.debian.org/LSBInitScripts/DependencyBasedBoot

For Arch alternatives, see `MediaGoblin - ArchLinux rc.d scripts by jpope`_ and
`Mediagoblin init script on Archlinux by Chimo`_.

.. _`MediaGoblin - ArchLinux rc.d scripts by jpope`: http://whird.jpope.org/2012/04/14/mediagoblin-archlinux-rcd-scripts
.. _`Mediagoblin init script on Archlinux by Chimo`: http://chimo.chromic.org/2012/03/01/mediagoblin-init-script-on-archlinux/

Installation
------------

1. Download the ``mediagoblin-paster.sh`` script.
2. Open the ``mediagoblin-paster.sh`` script in your favourite text editor.
3. Replace ``MG_ROOT=...`` and ``MG_USER=...`` with values that fit your
   environment.
4. Save the script to ``/etc/init.d/mediagoblin-paster`` (without the ``.sh``
   file extension)
5. Run ``sudo insserv mediagoblin-paster``.
6. *Repeat all steps again, but with mediagoblin-celeryd.*

Now, to start the services, simply run 
``sudo service mediagoblin-paster start`` and
``sudo service mediagoblin-celeryd start``.

License
-------
See LICENSE
