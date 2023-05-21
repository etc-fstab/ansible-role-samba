Role Name
=========
The samba role manages:

- Samba packages
- Samba services
- /etc/samba/smb.conf
- /etc/samba/shares.conf

Above assumes /etc/samba/smb.conf has line "include /etc/samba/shares.conf",
this can be re-designed to meet your use cases. 

The role supports various use cases where you can define:

- Ansible OS family running Samba (ex. some os/distro in your company don't run/support Samba)
- Host based Samba conf (ex, a host has specific/unique samba conf)
- Group of hosts running Samba (ex, a group of hosts has unique samba conf)
- Common default is 'no', meaning if no host/hostgroup samba cfg, the role won't configure samnba on a common host. 

Requirements
------------
None

Role Variables
--------------

- Distro vars:

```samba_mgmt_by_family```
```samba_packages```
```samba_services```

- Host or hostgroup vars:

```samba_mgmt_by_unit```
```etc_samba_smb_conf```
```etc_samba_shares_conf```


Dependencies
------------
None

Example Playbook
----------------
See tests folder.

Author Information
-----------------
ZD

License
---------
Public domain. No ownership such as copyright, trademark, patent. No warranty.
