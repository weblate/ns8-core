# NetBIOS domain name Schema

```txt
http://schema.nethserver.org/samba/configure-module-input.json#/properties/nbdomain
```



| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [configure-module-input.json\*](samba/configure-module-input.json "open original schema") |

## nbdomain Type

`string` ([NetBIOS domain name](configure-module-input-properties-netbios-domain-name.md))

## nbdomain Constraints

**maximum length**: the maximum number of characters for this string is: `15`

**minimum length**: the minimum number of characters for this string is: `1`

**pattern**: the string must match the following regular expression:&#x20;

```regexp
^[a-zA-Z][-a-zA-Z0-9]*$
```

[try pattern](https://regexr.com/?expression=%5E%5Ba-zA-Z%5D%5B-a-zA-Z0-9%5D*%24 "try regular expression with regexr.com")
