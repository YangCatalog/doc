# Yang Catalog tool documentation

This repository contains global documentation of the Yang Catalog tool (including several configuration files).

## Configuration files

### yangcatalog.conf

This is the main configuration file to be customized and placed in /etc/yangcatalog directory. It contains all directories, credentials (so beware of the read access), URI, ...

### yangcatalog.dns

It is the DNS zone file for yangcatalog.org

### yang_logrotate

This file should be placed into  /etc/logrotate.d/ in order to have a daily rotation (and compression) of all log files.

### yangcatalog-tmpfiles.conf

This file should be placed into /etc/tmpdfiles.d/ in order to create the required /run/yang and /var/yang/logs at boot time.

## Other repositoires

### backend repository

It contains all scripts implementing the REST API to the YangCatalog.

### sdo_analysis repository

It contains the tools to extract the YANG modules from IETF documents (RFC and drafts), from the [https://github.com/YangModels] global YANG modules catalog.

### search repository

It contains all Django scripts implementing the YangSearch part of the YangCatalog.

### web_root repository

It contains all static web content of https://yangcatalog.org

## pyang additional modules

Three files must be added in `/usr/local/lib/python3.6/dist-packages/pyang/plugins` (or where PYANG was installed):

- json-tree.py
- yang-catalog-index.py

All those plugins are in the search repository in scripts/pyang_plugins directory.

## libyang

Must be installed from git clone https://github.com/CESNET/libyang.git
