# Untitled object in Facts Schema validation Schema

```txt
https://schema.nethserver.org/facts/2022-12.json#/$defs/cluster-facts
```

NS8 Agent Facts.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                  |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [2022-12.json\*](facts/2022-12.json "open original schema") |

## cluster-facts Type

`object` ([Details](2022-12-defs-cluster-facts.md))

# cluster-facts Properties

| Property            | Type     | Required | Nullable       | Defined by                                                                                                                                                             |
| :------------------ | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [cluster](#cluster) | `object` | Required | cannot be null | [Facts Schema validation](2022-12-defs-cluster-facts-properties-cluster.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/cluster-facts/properties/cluster") |
| [nodes](#nodes)     | `object` | Required | cannot be null | [Facts Schema validation](2022-12-defs-cluster-facts-properties-nodes.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/cluster-facts/properties/nodes")     |
| [modules](#modules) | `object` | Required | cannot be null | [Facts Schema validation](2022-12-defs-cluster-facts-properties-modules.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/cluster-facts/properties/modules") |

## cluster

Facts from the cluster.

`cluster`

*   is required

*   Type: `object` ([Details](2022-12-defs-cluster-facts-properties-cluster.md))

*   cannot be null

*   defined in: [Facts Schema validation](2022-12-defs-cluster-facts-properties-cluster.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/cluster-facts/properties/cluster")

### cluster Type

`object` ([Details](2022-12-defs-cluster-facts-properties-cluster.md))

## nodes

Facts from nodes in the cluster.

`nodes`

*   is required

*   Type: `object` ([Details](2022-12-defs-cluster-facts-properties-nodes.md))

*   cannot be null

*   defined in: [Facts Schema validation](2022-12-defs-cluster-facts-properties-nodes.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/cluster-facts/properties/nodes")

### nodes Type

`object` ([Details](2022-12-defs-cluster-facts-properties-nodes.md))

### nodes Constraints

**minimum number of properties**: the minimum number of properties for this object is: `1`

## modules

Facts from modules.

`modules`

*   is required

*   Type: `object` ([Details](2022-12-defs-cluster-facts-properties-modules.md))

*   cannot be null

*   defined in: [Facts Schema validation](2022-12-defs-cluster-facts-properties-modules.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/cluster-facts/properties/modules")

### modules Type

`object` ([Details](2022-12-defs-cluster-facts-properties-modules.md))
