# ansible-spectrum-protect

A simple playbook that will check if node is registered based on inventory servers, if not found it will be registered on least utilized server based on storage.

Theres some extra variables required to start the playbook, such as client_fqdn and domain etc...

```
ansible-playbook main.yml --extra-vars="client_fqdn=test.sam.local domain=bronze_ba cloptset=windows customer=test" --ask-vault-pass

```

## Ansible Vault

vars/global_vars.yml contains vault variables. Use the correct vault secret i AWX or --vault-secret when running the playbook.

## dsmadmc

this play book use spectrum agent tools to run, and depends on the dsm.sys to be correctly configured on agent node.
