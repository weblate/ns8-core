# update-module input Schema

```txt
http://schema.nethserver.org/cluster/update-module-input.json
```

Input schema of the update-module action

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                          |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [update-module-input.json](cluster/update-module-input.json "open original schema") |

## update-module input Type

`object` ([update-module input](update-module-input.md))

## update-module input Examples

```json
{
  "module_url": "ghcr.io/nethserver/mymodule:3.2.2",
  "instances": [
    "mymodule2",
    "mymodule3"
  ]
}
```

```json
{
  "instances": [
    "mymodule2",
    "mymodule3"
  ]
}
```

# update-module input Properties

| Property                   | Type     | Required | Nullable       | Defined by                                                                                                                                                 |
| :------------------------- | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [module\_url](#module_url) | `string` | Optional | cannot be null | [update-module input](update-module-input-properties-module_url.md "http://schema.nethserver.org/cluster/update-module-input.json#/properties/module_url") |
| [instances](#instances)    | `array`  | Required | cannot be null | [update-module input](update-module-input-properties-instances.md "http://schema.nethserver.org/cluster/update-module-input.json#/properties/instances")   |

## module\_url

Module image URL to download and install. If empty, search for the latest available image from repositories.

`module_url`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [update-module input](update-module-input-properties-module_url.md "http://schema.nethserver.org/cluster/update-module-input.json#/properties/module_url")

### module\_url Type

`string`

## instances

Instance identifiers where the selected image is installed

`instances`

*   is required

*   Type: `string[]`

*   cannot be null

*   defined in: [update-module input](update-module-input-properties-instances.md "http://schema.nethserver.org/cluster/update-module-input.json#/properties/instances")

### instances Type

`string[]`

### instances Constraints

**minimum number of items**: the minimum number of items for this array is: `1`
