Role Name
=========

Use this Role to Add A Chain Template to the ISAM Appliance.

Requirements
------------
N/A

Role Variables
--------------

Provide the name, description (optional), and chain items of the new chain template
```
  chain_template_name: Template 1
  chain_template_description: Description for Template 1
  chain_template_items:
    - {"id": "default-map", "mode": "map", "prefix": "my-map"}
    - {"id": "default-saml2_0", "mode": "issue", "prefix": "my-saml2_0"}
```

The role automatically takes a snapshot before adding the chain template, override as needed:
`add_chain_template_comment: "Automated Snapshot Before Adding Chain Template"`

Dependencies
------------
N/A

Example Playbook
----------------

Here is an example of how to use this role:

    - hosts: servers
      connection: local
      roles:
         - role: ibm.isam.add_chain_template
           chain_template_name: Template 1
           chain_template_description: Description for Template 1
           chain_template_items:
             - {"id": "default-map", "mode": "map", "prefix": "my-map"}
             - {"id": "default-saml2_0", "mode": "issue", "prefix": "my-saml2_0"}

License
-------

Apache

Author Information
------------------

Ryan Dunn (rdunn1121@gmail.com)
