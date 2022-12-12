# Untitled string in Facts Schema validation Schema

```txt
https://schema.nethserver.org/facts/2022-12.json#/$defs/host-info/properties/version
```

Version of the phoning software that runs on the machine.

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                  |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [2022-12.json\*](facts/2022-12.json "open original schema") |

## version Type

`string`

## version Constraints

**pattern**: the string must match the following regular expression:&#x20;

```regexp
^\d+\.\d+\.?\d*$
```

[try pattern](https://regexr.com/?expression=%5E%5Cd%2B%5C.%5Cd%2B%5C.%3F%5Cd*%24 "try regular expression with regexr.com")
