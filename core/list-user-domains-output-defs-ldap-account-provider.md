# LDAP account provider Schema

```txt
http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider
```

An LDAP account provider is a database of users and groups that can also be used as an authentication backend. A user domain is composed by at least one LDAP account provider. Multiple replicas can be instantiated on different cluster nodes.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                     |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [list-user-domains-output.json*](cluster/list-user-domains-output.json "open original schema") |

## ldap-provider Type

`object` ([LDAP account provider](list-user-domains-output-defs-ldap-account-provider.md))

# ldap-provider Properties

| Property            | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                         |
| :------------------ | :-------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id)           | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-id.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/id")           |
| [ui_name](#ui_name) | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-ui_name.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/ui_name") |
| [node](#node)       | `integer` | Required | can be null    | [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-node.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/node")       |
| [host](#host)       | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-host.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/host")       |
| [port](#port)       | `integer` | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-port.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/port")       |

## id



`id`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-id.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/id")

### id Type

`string`

### id Constraints

**minimum length**: the minimum number of characters for this string is: `1`

## ui_name



`ui_name`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-ui_name.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/ui_name")

### ui_name Type

`string`

## node



`node`

*   is required

*   Type: `integer`

*   can be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-node.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/node")

### node Type

`integer`

### node Constraints

**minimum**: the value of this number must greater than or equal to: `1`

## host



`host`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-host.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/host")

### host Type

`string`

### host Constraints

**minimum length**: the minimum number of characters for this string is: `1`

## port



`port`

*   is required

*   Type: `integer`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-port.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/port")

### port Type

`integer`

### port Constraints

**minimum**: the value of this number must greater than or equal to: `1`
