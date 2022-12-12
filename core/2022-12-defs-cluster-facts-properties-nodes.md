# Untitled object in Facts Schema validation Schema

```txt
https://schema.nethserver.org/facts/2022-12.json#/$defs/cluster-facts/properties/nodes
```

Facts from nodes in the cluster.

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                  |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [2022-12.json\*](facts/2022-12.json "open original schema") |

## nodes Type

`object` ([Details](2022-12-defs-cluster-facts-properties-nodes.md))

## nodes Constraints

**minimum number of properties**: the minimum number of properties for this object is: `1`

# nodes Properties

| Property | Type     | Required | Nullable       | Defined by                                                                                                                                                         |
| :------- | :------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `.*`     | `object` | Optional | cannot be null | [Facts Schema validation](2022-12-defs-host-info.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/cluster-facts/properties/nodes/patternProperties/.*") |

## Pattern: `.*`

Common information to be fetched per-host.

`.*`

*   is optional

*   Type: `object` ([Details](2022-12-defs-host-info.md))

*   cannot be null

*   defined in: [Facts Schema validation](2022-12-defs-host-info.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/cluster-facts/properties/nodes/patternProperties/.*")

### .\* Type

`object` ([Details](2022-12-defs-host-info.md))
