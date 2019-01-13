Role Name
=========

This role will install Informix, from a single node, to a MACH-11 cluster, with or without a configurable number of Connection Managers.

Because of the complexity of the cluster, if you try and run this against an existing cluster, it will just abort wherever it sensibly can. This isn't currently intended to add nodes to a cluster, a future version or separate role might do that.

Similiarly, if you want to upgrade, you will need a different role, which is also in the pipeline.

Future releases might also ddress ER and Grid. Might.

Requirements
------------

It may be stating the obvious, but this does require your own licensed version(s) of Informix. No Informix is supplied with this role.

This has only been tested with HCL Informix, but I can't imagine any reason IBM Informix wouldn't work.

ole Variables
--------------

You will need to set up your Ansible hosts files with the groups specified.

You may want to change the Informix version information variable if you have multiple possible versions of Informix available in the relevant directory.

Similarly, you may also want to change the Informix media file name variable.

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

No other Ansible Galaxy roles are used at this time.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

MIT

Author Information
------------------

https://github.com/SpokeyWheeler
