# openldap

TODO - Draft

## Provision

Add a node to a domain:

    api-cli run provision-domain --agent module/openldap1 --data - <<EOF
    {
        "adminuser":"admin",
        "adminpass":"Nethesis,1234",
        "domain":"$(hostname -d)"
    }
    EOF

Further OpenLDAP instances for the same `domain` are **joined** together
in a multi-master cluster. The command is almost the same: just change the
`--agent` argument, e.g. `--agent module/openldap2` and so on.

Admin credentials can be set differently for each instance.
