# get-defaults input Schema

```txt
http://schema.nethserver.org/samba/get-defaults-input.json
```

Compute the values that suit the configure-module action input

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                      |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [get-defaults-input.json](samba/get-defaults-input.json "open original schema") |

## get-defaults input Type

`object` ([get-defaults input](get-defaults-input.md))

# get-defaults input Properties

| Property                | Type     | Required | Nullable       | Defined by                                                                                                                                          |
| :---------------------- | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| [provision](#provision) | `string` | Required | cannot be null | [get-defaults input](get-defaults-input-properties-provision.md "http://schema.nethserver.org/samba/get-defaults-input.json#/properties/provision") |
| [realm](#realm)         | `string` | Optional | cannot be null | [get-defaults input](get-defaults-input-properties-domain-name.md "http://schema.nethserver.org/samba/get-defaults-input.json#/properties/realm")   |

## provision



`provision`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [get-defaults input](get-defaults-input-properties-provision.md "http://schema.nethserver.org/samba/get-defaults-input.json#/properties/provision")

### provision Type

`string`

### provision Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value           | Explanation |
| :-------------- | :---------- |
| `"new-domain"`  |             |
| `"join-domain"` |             |

## realm

Can be `null` if `provision` is `new-domain`

`realm`

*   is optional

*   Type: `string` ([Domain name](get-defaults-input-properties-domain-name.md))

*   cannot be null

*   defined in: [get-defaults input](get-defaults-input-properties-domain-name.md "http://schema.nethserver.org/samba/get-defaults-input.json#/properties/realm")

### realm Type

`string` ([Domain name](get-defaults-input-properties-domain-name.md))

### realm Constraints

**maximum length**: the maximum number of characters for this string is: `140`

**minimum length**: the minimum number of characters for this string is: `1`

**pattern**: the string must match the following regular expression:&#x20;

```regexp
^[a-zA-Z][-a-zA-Z0-9]{0,62}(\.[a-zA-Z][-a-zA-Z0-9]{0,62})+$
```

[try pattern](https://regexr.com/?expression=%5E%5Ba-zA-Z%5D%5B-a-zA-Z0-9%5D%7B0%2C62%7D\(%5C.%5Ba-zA-Z%5D%5B-a-zA-Z0-9%5D%7B0%2C62%7D\)%2B%24 "try regular expression with regexr.com")

# get-defaults input Definitions
