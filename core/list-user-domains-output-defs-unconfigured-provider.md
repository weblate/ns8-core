# Unconfigured provider Schema

```txt
http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider
```

An internal provider module instance that is not completely configured

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                     |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [list-user-domains-output.json*](cluster/list-user-domains-output.json "open original schema") |

## unconfigured-provider Type

`object` ([Unconfigured provider](list-user-domains-output-defs-unconfigured-provider.md))

# unconfigured-provider Properties

| Property                  | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                                              |
| :------------------------ | :-------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [module_id](#module_id)   | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-module-identifier.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/module_id")  |
| [node](#node)             | `integer` | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-node-identifier.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/node")         |
| [image_name](#image_name) | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-module-image-name.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/image_name") |
| [image_url](#image_url)   | `string`  | Required | cannot be null | [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-image-url.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/image_url")          |

## module_id

e.g. `samba1`

`module_id`

*   is required

*   Type: `string` ([Module identifier](list-user-domains-output-defs-unconfigured-provider-properties-module-identifier.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-module-identifier.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/module_id")

### module_id Type

`string` ([Module identifier](list-user-domains-output-defs-unconfigured-provider-properties-module-identifier.md))

## node

The node number, e.g. `1`

`node`

*   is required

*   Type: `integer` ([Node identifier](list-user-domains-output-defs-unconfigured-provider-properties-node-identifier.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-node-identifier.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/node")

### node Type

`integer` ([Node identifier](list-user-domains-output-defs-unconfigured-provider-properties-node-identifier.md))

### node Constraints

**minimum**: the value of this number must greater than or equal to: `1`

## image_name

e.g. `samba`

`image_name`

*   is required

*   Type: `string` ([Module image name](list-user-domains-output-defs-unconfigured-provider-properties-module-image-name.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-module-image-name.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/image_name")

### image_name Type

`string` ([Module image name](list-user-domains-output-defs-unconfigured-provider-properties-module-image-name.md))

## image_url

ghcr.io/nethserver/samba:2.0.0

`image_url`

*   is required

*   Type: `string` ([Image URL](list-user-domains-output-defs-unconfigured-provider-properties-image-url.md))

*   cannot be null

*   defined in: [list-user-domains output](list-user-domains-output-defs-unconfigured-provider-properties-image-url.md "http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/unconfigured-provider/properties/image_url")

### image_url Type

`string` ([Image URL](list-user-domains-output-defs-unconfigured-provider-properties-image-url.md))
