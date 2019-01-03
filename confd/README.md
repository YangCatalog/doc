# confd directory

This directory contains all files required to run Cisco Tail-F ConfD.

  - *confd.service-dist*: to be customized and linked/copied for `/etc/systems/system/confd.service`. This service definition is for `systemd` start--up and should probably be enabled and started by `systemctl`.
  - *confd.conf-dist*: to be customized and placed in the directory mentionned in the above file.
  - * .yang *: all yang files required for Yang Catalog
  - *yangcatalog_aaa_init.xml-dist*: to be customized to contain the local credentials for the web API to ConfD
