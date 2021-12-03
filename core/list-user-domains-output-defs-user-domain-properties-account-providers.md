# Account providers Schema

```txt
http://schema.nethserver.org/cluster/list-user-domains-output.json#/$defs/user-domain/properties/providers
```

Backend system and replicas providing the services of the user domain

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                     |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [list-user-domains-output.json*](cluster/list-user-domains-output.json "open original schema") |

## providers Type

`array` ([Account providers](list-user-domains-output-defs-user-domain-properties-account-providers.md))

## providers Constraints

**minimum number of items**: the minimum number of items for this array is: `1`
