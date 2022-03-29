# remove-internal-provider input Schema

```txt
http://schema.nethserver.org/cluster/remove-internal-provider-input.json
```

Safely remove a user domain provider.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [remove-internal-provider-input.json](cluster/remove-internal-provider-input.json "open original schema") |

## remove-internal-provider input Type

`object` ([remove-internal-provider input](remove-internal-provider-input.md))

## remove-internal-provider input Examples

```json
{
  "module_id": "samba1"
}
```

# remove-internal-provider input Properties

| Property                 | Type     | Required | Nullable       | Defined by                                                                                                                                                                                        |
| :----------------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [module\_id](#module_id) | `string` | Required | cannot be null | [remove-internal-provider input](remove-internal-provider-input-properties-module-identifier.md "http://schema.nethserver.org/cluster/remove-internal-provider-input.json#/properties/module_id") |

## module\_id



`module_id`

*   is required

*   Type: `string` ([Module identifier](remove-internal-provider-input-properties-module-identifier.md))

*   cannot be null

*   defined in: [remove-internal-provider input](remove-internal-provider-input-properties-module-identifier.md "http://schema.nethserver.org/cluster/remove-internal-provider-input.json#/properties/module_id")

### module\_id Type

`string` ([Module identifier](remove-internal-provider-input-properties-module-identifier.md))

### module\_id Constraints

**minimum length**: the minimum number of characters for this string is: `1`
