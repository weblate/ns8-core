# list-user-domains output Schema

```txt
http://schema.nethserver.org/cluster/list-user-domains-output.json
```

Quickly get the user domains list and their basic configuration

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                    |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [list-user-domains-output.json](cluster/list-user-domains-output.json "open original schema") |

## list-user-domains output Type

`object` ([list-user-domains output](list-user-domains-output.md))

## list-user-domains output Examples

```json
{
  "unconfigured_providers": [
    {
      "module_id": "samba1",
      "image_name": "samba",
      "image_url": "ghcr.io/nethserver/samba:latest"
    }
  ],
  "domains": [
    {
      "name": "sandbox.example",
      "location": "internal",
      "protocol": "ldap",
      "schema": "rfc2307",
      "base_dn": "dc=sandbox,dc=example",
      "bind_dn": "cn=ldapservice,dc=sandbox,dc=example",
      "bind_password": "S3cr3t!",
      "tls": false,
      "tls_verify": false,
      "providers": [
        {
          "id": "openldap1",
          "ui_name": "",
          "node": 1,
          "host": "10.110.32.2",
          "port": 20003
        },
        {
          "id": "openldap2",
          "ui_name": "",
          "node": 2,
          "host": "10.110.32.3",
          "port": 20002
        }
      ]
    },
    {
      "name": "company.org",
      "location": "external",
      "protocol": "ldap",
      "schema": "rfc2307",
      "base_dn": "dc=company,dc=org",
      "bind_dn": "cn=ns8cluster,dc=company,dc=org",
      "bind_password": "OtherS3cr3t!",
      "tls": true,
      "tls_verify": true,
      "providers": [
        {
          "id": "ldap-primary.company.org",
          "ui_name": "Company LDAP primary",
          "node": null,
          "host": "ldap-master.company.org",
          "port": 636
        },
        {
          "id": "ldap-replica.company.org",
          "ui_name": "Company LDAP replica",
          "node": null,
          "host": "ldap-replica.company.org",
          "port": 636
        }
      ]
    }
  ]
}
```

# list-user-domains output Properties

| Property                                          | Type    | Required | Nullable       | Defined by                                                                                                                                                                                        |
| :------------------------------------------------ | :------ | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [unconfigured_providers](#unconfigured_providers) | `array` | Required | cannot be null | [list-user-domains output](list-user-domains-output-properties-unconfigured_providers.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/properties/unconfigured_providers") |
| [domains](#domains)                               | `array` | Required | cannot be null | [list-user-domains output](list-user-domains-output-properties-domains.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/properties/domains")                               |

## unconfigured_providers



`unconfigured_providers`

*   is required

*   Type: `object[]` ([Unconfigured provider](list-user-domains-output-defs-unconfigured-provider.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-properties-unconfigured_providers.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/properties/unconfigured_providers")

### unconfigured_providers Type

`object[]` ([Unconfigured provider](list-user-domains-output-defs-unconfigured-provider.md))

## domains



`domains`

*   is required

*   Type: `object[]` ([User domain](list-user-domains-output-defs-user-domain.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-properties-domains.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/properties/domains")

### domains Type

`object[]` ([User domain](list-user-domains-output-defs-user-domain.md))

### domains Constraints

**minimum number of items**: the minimum number of items for this array is: `0`

# list-user-domains output Definitions

## Definitions group user-domain

Reference this group by using

```json
{"$ref":"http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/user-domain"}
```

| Property                | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                              |
| :---------------------- | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)           | `string` | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-user-domain-properties-name.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/user-domain/properties/name")                        |
| [location](#location)   | `string` | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-user-domain-properties-domain-hosting-location.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/user-domain/properties/location") |
| [protocol](#protocol)   | `string` | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-user-domain-properties-provider-protocol.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/user-domain/properties/protocol")       |
| [providers](#providers) | `array`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-user-domain-properties-account-providers.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/user-domain/properties/providers")      |

### name



`name`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-user-domain-properties-name.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/user-domain/properties/name")

#### name Type

`string`

#### name Constraints

**minimum length**: the minimum number of characters for this string is: `1`

### location

Type of domain hosting. Set to `internal` if the domain is hosted by the cluster, `external` if the domain is provided by a remote service

`location`

*   is required

*   Type: `string` ([Domain hosting location](list-user-domains-output-defs-user-domain-properties-domain-hosting-location.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-user-domain-properties-domain-hosting-location.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/user-domain/properties/location")

#### location Type

`string` ([Domain hosting location](list-user-domains-output-defs-user-domain-properties-domain-hosting-location.md))

#### location Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value        | Explanation |
| :----------- | :---------- |
| `"internal"` |             |
| `"external"` |             |

### protocol

Protocol used to communicate with the domain providers.

`protocol`

*   is required

*   Type: `string` ([Provider protocol](list-user-domains-output-defs-user-domain-properties-provider-protocol.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-user-domain-properties-provider-protocol.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/user-domain/properties/protocol")

#### protocol Type

`string` ([Provider protocol](list-user-domains-output-defs-user-domain-properties-provider-protocol.md))

#### protocol Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value    | Explanation |
| :------- | :---------- |
| `"ldap"` |             |

### providers

Backend system and replicas providing the services of the user domain

`providers`

*   is required

*   Type: `array` ([Account providers](list-user-domains-output-defs-user-domain-properties-account-providers.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-user-domain-properties-account-providers.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/user-domain/properties/providers")

#### providers Type

`array` ([Account providers](list-user-domains-output-defs-user-domain-properties-account-providers.md))

#### providers Constraints

**minimum number of items**: the minimum number of items for this array is: `1`

## Definitions group unconfigured-provider

Reference this group by using

```json
{"$ref":"http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider"}
```

| Property                  | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                                              |
| :------------------------ | :-------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [module_id](#module_id)   | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-module-identifier.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/module_id")  |
| [node](#node)             | `integer` | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-node-identifier.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/node")         |
| [image_name](#image_name) | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-module-image-name.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/image_name") |
| [image_url](#image_url)   | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-image-url.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/image_url")          |

### module_id

e.g. `samba1`

`module_id`

*   is required

*   Type: `string` ([Module identifier](list-user-domains-output-defs-unconfigured-provider-properties-module-identifier.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-module-identifier.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/module_id")

#### module_id Type

`string` ([Module identifier](list-user-domains-output-defs-unconfigured-provider-properties-module-identifier.md))

### node

The node number, e.g. `1`

`node`

*   is required

*   Type: `integer` ([Node identifier](list-user-domains-output-defs-unconfigured-provider-properties-node-identifier.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-node-identifier.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/node")

#### node Type

`integer` ([Node identifier](list-user-domains-output-defs-unconfigured-provider-properties-node-identifier.md))

#### node Constraints

**minimum**: the value of this number must greater than or equal to: `1`

### image_name

e.g. `samba`

`image_name`

*   is required

*   Type: `string` ([Module image name](list-user-domains-output-defs-unconfigured-provider-properties-module-image-name.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-module-image-name.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/image_name")

#### image_name Type

`string` ([Module image name](list-user-domains-output-defs-unconfigured-provider-properties-module-image-name.md))

### image_url

ghcr.io/nethserver/samba:2.0.0

`image_url`

*   is required

*   Type: `string` ([Image URL](list-user-domains-output-defs-unconfigured-provider-properties-image-url.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-image-url.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/image_url")

#### image_url Type

`string` ([Image URL](list-user-domains-output-defs-unconfigured-provider-properties-image-url.md))

## Definitions group ldap-provider

Reference this group by using

```json
{"$ref":"http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider"}
```

| Property            | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                         |
| :------------------ | :-------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id)           | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-id.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/id")           |
| [ui_name](#ui_name) | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-ui_name.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/ui_name") |
| [node](#node-1)     | `integer` | Required | can be null    | [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-node.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/node")       |
| [host](#host)       | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-host.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/host")       |
| [port](#port)       | `integer` | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-port.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/port")       |

### id



`id`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-id.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/id")

#### id Type

`string`

#### id Constraints

**minimum length**: the minimum number of characters for this string is: `1`

### ui_name



`ui_name`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-ui_name.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/ui_name")

#### ui_name Type

`string`

### node



`node`

*   is required

*   Type: `integer`

*   can be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-node.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/node")

#### node Type

`integer`

#### node Constraints

**minimum**: the value of this number must greater than or equal to: `1`

### host



`host`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-host.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/host")

#### host Type

`string`

#### host Constraints

**minimum length**: the minimum number of characters for this string is: `1`

### port



`port`

*   is required

*   Type: `integer`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-account-provider-properties-port.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/ldap-provider/properties/port")

#### port Type

`integer`

#### port Constraints

**minimum**: the value of this number must greater than or equal to: `1`

## Definitions group additional-properties-of-ldap

Reference this group by using

```json
{"$ref":"http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap"}
```

| Property                        | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                                                      |
| :------------------------------ | :-------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [schema](#schema)               | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-ldap-database-schema.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/schema") |
| [base_dn](#base_dn)             | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-base_dn.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/base_dn")             |
| [bind_dn](#bind_dn)             | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-bind_dn.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/bind_dn")             |
| [bind_password](#bind_password) | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-bind_password.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/bind_password") |
| [tls](#tls)                     | `boolean` | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-tls.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/tls")                     |
| [tls_verify](#tls_verify)       | `boolean` | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-tls_verify.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/tls_verify")       |

### schema



`schema`

*   is required

*   Type: `string` ([LDAP database schema](list-user-domains-output-defs-ldap-domain-properties-properties-ldap-database-schema.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-ldap-database-schema.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/schema")

#### schema Type

`string` ([LDAP database schema](list-user-domains-output-defs-ldap-domain-properties-properties-ldap-database-schema.md))

#### schema Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value       | Explanation |
| :---------- | :---------- |
| `"ad"`      |             |
| `"rfc2307"` |             |

### base_dn



`base_dn`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-base_dn.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/base_dn")

#### base_dn Type

`string`

#### base_dn Constraints

**minimum length**: the minimum number of characters for this string is: `1`

### bind_dn



`bind_dn`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-bind_dn.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/bind_dn")

#### bind_dn Type

`string`

#### bind_dn Constraints

**minimum length**: the minimum number of characters for this string is: `1`

### bind_password



`bind_password`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-bind_password.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/bind_password")

#### bind_password Type

`string`

#### bind_password Constraints

**minimum length**: the minimum number of characters for this string is: `1`

### tls



`tls`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-tls.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/tls")

#### tls Type

`boolean`

### tls_verify



`tls_verify`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-ldap-domain-properties-properties-tls_verify.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/additional-properties-of-ldap/properties/tls_verify")

#### tls_verify Type

`boolean`
