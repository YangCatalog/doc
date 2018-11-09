# Yang Catalog tool documentation

This repository contains global documentation of the Yang Catalog tool (including configuration file).

## yangcatalog.conf

This is the main configuration file to be customized and placed in /etc/yangcatalog directory. It contains all directories, credentials (so beware of the read access), URI, ...

## sdo_analysis repository

It contains the tools to extract the YANG modules from IETF documents (RFC and drafts), from the [https://github.com/YangModels] global YANG modules catalog.

## yang (in logrotate)

The /etc/logrotate.d/yang should contain:
```
/var/yang/logs/yang.log {
    rotate 7
    daily
    compress
    missingok
    copytruncate
}
/var/yang/logs/uwsgi/*.log {
    rotate 7
    daily
    compress
    missingok
    copytruncate
} 
```

## pyang additional modules

Three files must be added in `/usr/local/lib/python3.6/dist-packages/pyang/plugins` (or where PYANG was installed):

- json-tree.py
- name-revision.py or name.py ?
- yang-catalog-index.py 

## libyang

Must be installed from git clone https://github.com/CESNET/libyang.git
