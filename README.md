raspi-unbound-resolver
=========

Installs and configures NLNetLabs' unbound as a recursive nameserver

Requirements
------------

You should put your locally edited unbound.conf in {{ inventory_dir }}/host_files/{{ inventory_hostname }}.

If you don't, you'll get a default one which is about enough to get unbound to start.

Role Variables
--------------

raspi_unbound_void_zones - define this if you want https://github.com/cyclaero/void-zones-tools
Note that you still have to include the output of this tool in unbound.conf if you want
it to actually block the zones.  A good place to do this might be in {{ inventory_dir }}/group_vars/all.yml
or maybe in {{ inventory_dir }}/host_vars/something.yml


for your requirements.yml:

- src: https://github.com/res3066/ansiblerole-raspi-apcupsd
  name: raspi-apcupsd
  scm: git


Dependencies
------------

Potentially, https://github.com/cyclaero/void-zones-tools



Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - raspi-apcupsd

License
-------

MIT

Author Information
------------------

Rob Seastrom <rs@seastrom.com>

