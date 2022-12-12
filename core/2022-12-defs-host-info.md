# Untitled object in Facts Schema validation Schema

```txt
https://schema.nethserver.org/facts/2022-12.json#/$defs/host-info
```

Common information to be fetched per-host.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                  |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [2022-12.json\*](facts/2022-12.json "open original schema") |

## host-info Type

`object` ([Details](2022-12-defs-host-info.md))

# host-info Properties

| Property            | Type     | Required | Nullable       | Defined by                                                                                                                                                     |
| :------------------ | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [version](#version) | `string` | Required | cannot be null | [Facts Schema validation](2022-12-defs-host-info-properties-version.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/host-info/properties/version") |
| [distro](#distro)   | `object` | Required | cannot be null | [Facts Schema validation](2022-12-defs-host-info-properties-distro.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/host-info/properties/distro")   |

## version

Version of the phoning software that runs on the machine.

`version`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [Facts Schema validation](2022-12-defs-host-info-properties-version.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/host-info/properties/version")

### version Type

`string`

### version Constraints

**pattern**: the string must match the following regular expression:&#x20;

```regexp
^\d+\.\d+\.?\d*$
```

[try pattern](https://regexr.com/?expression=%5E%5Cd%2B%5C.%5Cd%2B%5C.%3F%5Cd*%24 "try regular expression with regexr.com")

## distro

Distribution that the host runs on.

`distro`

*   is required

*   Type: `object` ([Details](2022-12-defs-host-info-properties-distro.md))

*   cannot be null

*   defined in: [Facts Schema validation](2022-12-defs-host-info-properties-distro.md "https://schema.nethserver.org/facts/2022-12.json#/$defs/host-info/properties/distro")

### distro Type

`object` ([Details](2022-12-defs-host-info-properties-distro.md))
