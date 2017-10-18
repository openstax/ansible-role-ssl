ansible-role-ssl
=========

This role is a dependency for [ansible_role_nginx](https://github.com/openstax/ansible-role-nginx) and allows the use of copying certs from a s3 bucket and hopefully in the future from a local directory.  

Currently (Oct 18, 2017), the way ssl certs are copied is from the deployment server. This doesn't allow us to use travis in order to conduct tests on the role. The downloading from an s3 bucket is problematic b/c then we need to install specific packages in order to manipulate the s3 bucket. This is not ideal either.

This role needs to be refactored to allow either of the methods mentioned above and possibly a 3rd method to replace them. If we copy the servers locally first and then use the copy method we can avoid the first two problems.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

GPLv2

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
