# confd directory

This directory contains all files required to run Cisco Tail-F ConfD.

  - *confd.service-dist*: to be localized and linked/copied for `/etc/systems/system/confd.service`. This service definition is for `systemd` start--up and should probably be enabled and started by `systemctl`.
  - *confd.conf-dist*: to be localized and placed in the directory mentionned in the above file.
  - * .yang *: all yang files required for Yang Catalog
