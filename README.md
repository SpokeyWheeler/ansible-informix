Informix
========

This role will (eventually) install Informix, from a single node, to an HDR and / or RSS cluster, with or without a configurable number of Connection Managers.

I've tried to make it CI-friendly, but that's a pretty vague requiremment.

Requirements
------------

It may be stating the obvious, but this does require your own licensed version(s) of Informix. No Informix is supplied with this role.

My focus has been on HCL Informix, but I have also tried to make sure IBM Informix will work. Furthermore, I've developed this using the very latest 12.10, but I can't see any reason that it wouldn't work for any currently supported version.

I have written this to work with Centos 7, but RHEL 7 and the equivalent Fedora should also work. I will try and get round to Debian / Ubuntu / OpenSuSE. 

It's expecting to use bash. Also, it uses systemd to manage the service.

Role Variables
--------------

You will need to set up your Ansible hosts files with the groups specified.

You may want to change the Informix version information variable if you have multiple possible versions of Informix available in the relevant directory.

Similarly, you may also want to change the Informix media file name variable.

You will also need to set your expected environment size, the default is "medium".

There are a number of standard configurations:

Small: Single-core, suitable for "departmental" workload

Medium: Quad-core, suitable for a couple of hundred OLTP users

Large: 16-core, suitable for large OLTP uses

Extra-large: 48-core, suitable for very large OLTP uses

Mixed-small: 16-core mixed OLTP / DSS use

Mixed-medium: 48-core mixed OLTP / DSS use

DSS-small: Quad-core, suitable for small DSS uses

DSS-medium: 16-core, suitable for medium DSS uses

DSS-large: 48-core, suitable for large DSS uses

There is a flag to enable Informix Warehouse Accelerator configuration

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

No other Ansible Galaxy roles are used at this time.

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: spokeywheeler.csdk }
         - { role: spokeywheeler.ids }
         - { role: spokeywheeler.jdbc }

License
-------

MIT

Author Information
------------------

<https://github.com/SpokeyWheeler>
