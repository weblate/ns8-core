# info-module input Schema

```txt
http://schema.nethserver.org/cluster/get-module-info-input.json
```

Retrieve the metadata information af a module

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                              |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [get-module-info-input.json](cluster/get-module-info-input.json "open original schema") |

## info-module input Type

`object` ([info-module input](get-module-info-input.md))

## info-module input Examples

```json
{
  "id": "dokuwiki"
}
```

# info-module input Properties

| Property  | Type     | Required | Nullable       | Defined by                                                                                                                                   |
| :-------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id) | `string` | Required | cannot be null | [info-module input](get-module-info-input-properties-id.md "http://schema.nethserver.org/cluster/get-module-info-input.json#/properties/id") |

## id

Module id

`id`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [info-module input](get-module-info-input-properties-id.md "http://schema.nethserver.org/cluster/get-module-info-input.json#/properties/id")

### id Type

`string`
