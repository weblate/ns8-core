# get-uuid output Schema

```txt
http://schema.nethserver.org/cluster/get-uuid-output.json
```

Output schema of the get-uuid action

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                  |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [get-uuid-output.json](cluster/get-uuid-output.json "open original schema") |

## get-uuid output Type

`object` ([get-uuid output](get-uuid-output.md))

## get-uuid output Examples

```json
{
  "uuid": "77365ea8-a2d6-4731-8a79-07e18e889e6a"
}
```

# get-uuid output Properties

| Property      | Type     | Required | Nullable       | Defined by                                                                                                                         |
| :------------ | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| [uuid](#uuid) | `string` | Required | cannot be null | [get-uuid output](get-uuid-output-properties-uuid.md "http://schema.nethserver.org/cluster/get-uuid-output.json#/properties/uuid") |

## uuid

Generated UUID

`uuid`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [get-uuid output](get-uuid-output-properties-uuid.md "http://schema.nethserver.org/cluster/get-uuid-output.json#/properties/uuid")

### uuid Type

`string`
