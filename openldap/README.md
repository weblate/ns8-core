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

## Setup

Enable server modules:

```
ldapadd -H ldapi:/// <<EOF
dn: cn=module,cn=config
cn: module 
objectClass: olcModuleList
olcModulePath: /opt/bitnami/openldap/lib/openldap/
olcModuleLoad: syncprov.so
EOF

dn: olcOverlay=syncprov,olcDatabase={2}mdb,cn=config
objectClass: olcOverlayConfig
objectClass: olcSyncProvConfig
olcOverlay: syncprov
```

Configure syncronization

```
ldapmodify -H ldapi:/// <<EOF
dn: cn=config
changetype: modify
replace: olcServerID
olcServerID: 2

dn: olcDatabase={2}mdb,cn=config
changetype:modify
replace: olcSyncrepl
olcSyncrepl: rid=001
  provider=ldap://10.5.4.1:20001
  binddn="cn=admin,dc=dp,dc=nethserver,dc=net"
  bindmethod=simple
  credentials=Nethesis,1234
  searchbase="dc=dp,dc=nethserver,dc=net"
  type=refreshAndPersist
  retry="5 5 300 +"
  timeout=5
-
replace: olcMirrorMode
olcMirrorMode: TRUE
EOF
```

Create the top level entry:

```
ldapadd -x -D cn=admin,dc=dp,dc=nethserver,dc=net -w Nethesis,1234 -H ldapi:///  <<EOF
dn: dc=dp,dc=nethserver,dc=net
objectClass: top
objectClass: dcObject
objectClass: organization
dc: dp
o: dp.nethserver.net
EOF
```