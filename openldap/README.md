# openldap

TODO - Draft

## Provision

Add a node to a domain:

    api-cli run provision-domain --agent module/openldap1 --data - <<EOF
    {
        "domain":"$(hostname -d)"
    }
    EOF

Further OpenLDAP instances for the same `domain` are **joined** together
in a multi-master cluster. The command is almost the same: just change the
`--agent` argument, e.g. `--agent module/openldap2` and so on.

## Setup

Enable server modules and configure syncronization:

```
ldapmodify -H ldapi:/// <<EOF

dn: cn=module,cn=config
changetype: add
cn: module
objectClass: olcModuleList
olcModulePath: /opt/bitnami/openldap/lib/openldap/
olcModuleLoad: syncprov.so

dn: olcOverlay=syncprov,olcDatabase={2}mdb,cn=config
changetype: add
objectClass: olcOverlayConfig
objectClass: olcSyncProvConfig
olcOverlay: syncprov

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

dn: ou=users,dc=dp,dc=nethserver,dc=net
objectClass: top
objectClass: organizationalUnit
ou: users

dn: ou=groups,dc=dp,dc=nethserver,dc=net
objectClass: top
objectClass: organizationalUnit
ou: groups

dn: cn=users,ou=groups,dc=dp,dc=nethserver,dc=net
objectClass: posixGroup
cn: users
gidNumber: 1000

dn: uid=admin,ou=users,dc=dp,dc=nethserver,dc=net
objectClass: posixAccount
gecos: Administrator
uid: admin
uidNumber: 1000
gidNumber: 1000
userPassword:: e0NSWVBUfSQ2JHJpSTQzenJ4VE1KWEcyNEIkc2t0WGNsa3JOUnN5ZG5OclFJa

EOF
```