# configure-module input Schema

```txt
http://schema.nethserver.org/samba/configure-module-input.json
```

Provision a Active Directory domain controller

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                              |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [configure-module-input.json](samba/configure-module-input.json "open original schema") |

## configure-module input Type

`object` ([configure-module input](configure-module-input.md))

any of

*   [Untitled undefined type in configure-module input](configure-module-input-anyof-0.md "check type definition")

*   [Untitled undefined type in configure-module input](configure-module-input-anyof-1.md "check type definition")

## configure-module input Examples

```json
{
  "provision": "new-domain",
  "adminuser": "administrator",
  "adminpass": "Nethesis,1234",
  "realm": "AD.EXAMPLE.COM",
  "ipaddress": "10.15.21.100",
  "hostname": "dc1",
  "nbdomain": "AD"
}
```

```json
{
  "provision": "join-domain",
  "adminuser": "administrator",
  "adminpass": "Nethesis,1234",
  "realm": "AD.EXAMPLE.COM",
  "ipaddress": "10.15.21.100",
  "hostname": "dc1"
}
```

# configure-module input Properties

| Property                | Type     | Required | Nullable       | Defined by                                                                                                                                                               |
| :---------------------- | :------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [provision](#provision) | `string` | Optional | cannot be null | [configure-module input](configure-module-input-properties-provision.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/provision")          |
| [adminuser](#adminuser) | `string` | Optional | cannot be null | [configure-module input](configure-module-input-properties-adminuser.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/adminuser")          |
| [adminpass](#adminpass) | `string` | Optional | cannot be null | [configure-module input](configure-module-input-properties-adminpass.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/adminpass")          |
| [ipaddress](#ipaddress) | `string` | Optional | cannot be null | [configure-module input](configure-module-input-properties-ipaddress.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/ipaddress")          |
| [hostname](#hostname)   | `string` | Optional | cannot be null | [configure-module input](configure-module-input-properties-hostname.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/hostname")            |
| [realm](#realm)         | `string` | Optional | cannot be null | [configure-module input](configure-module-input-properties-domain-name.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/realm")            |
| [nbdomain](#nbdomain)   | `string` | Optional | cannot be null | [configure-module input](configure-module-input-properties-netbios-domain-name.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/nbdomain") |

## provision



`provision`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [configure-module input](configure-module-input-properties-provision.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/provision")

### provision Type

`string`

### provision Constraints

**minimum length**: the minimum number of characters for this string is: `1`

## adminuser



`adminuser`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [configure-module input](configure-module-input-properties-adminuser.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/adminuser")

### adminuser Type

`string`

### adminuser Constraints

**minimum length**: the minimum number of characters for this string is: `1`

## adminpass



`adminpass`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [configure-module input](configure-module-input-properties-adminpass.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/adminpass")

### adminpass Type

`string`

### adminpass Constraints

**minimum length**: the minimum number of characters for this string is: `1`

## ipaddress



`ipaddress`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [configure-module input](configure-module-input-properties-ipaddress.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/ipaddress")

### ipaddress Type

`string`

### ipaddress Constraints

**IPv4**: the string must be an IPv4 address (dotted quad), according to [RFC 2673, section 3.2](https://tools.ietf.org/html/rfc2673 "check the specification")

## hostname



`hostname`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [configure-module input](configure-module-input-properties-hostname.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/hostname")

### hostname Type

`string`

### hostname Constraints

**maximum length**: the maximum number of characters for this string is: `15`

**pattern**: the string must match the following regular expression:&#x20;

```regexp
^[a-zA-Z][-a-zA-Z0-9]*$
```

[try pattern](https://regexr.com/?expression=%5E%5Ba-zA-Z%5D%5B-a-zA-Z0-9%5D*%24 "try regular expression with regexr.com")

## realm



`realm`

*   is optional

*   Type: `string` ([Domain name](configure-module-input-properties-domain-name.md))

*   cannot be null

*   defined in: [configure-module input](configure-module-input-properties-domain-name.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/realm")

### realm Type

`string` ([Domain name](configure-module-input-properties-domain-name.md))

### realm Constraints

**maximum length**: the maximum number of characters for this string is: `140`

**minimum length**: the minimum number of characters for this string is: `1`

**pattern**: the string must match the following regular expression:&#x20;

```regexp
^[a-zA-Z][-a-zA-Z0-9]{0,62}(\.[a-zA-Z][-a-zA-Z0-9]{0,62})+$
```

[try pattern](https://regexr.com/?expression=%5E%5Ba-zA-Z%5D%5B-a-zA-Z0-9%5D%7B0%2C62%7D\(%5C.%5Ba-zA-Z%5D%5B-a-zA-Z0-9%5D%7B0%2C62%7D\)%2B%24 "try regular expression with regexr.com")

## nbdomain



`nbdomain`

*   is optional

*   Type: `string` ([NetBIOS domain name](configure-module-input-properties-netbios-domain-name.md))

*   cannot be null

*   defined in: [configure-module input](configure-module-input-properties-netbios-domain-name.md "http://schema.nethserver.org/samba/configure-module-input.json#/properties/nbdomain")

### nbdomain Type

`string` ([NetBIOS domain name](configure-module-input-properties-netbios-domain-name.md))

### nbdomain Constraints

**maximum length**: the maximum number of characters for this string is: `15`

**minimum length**: the minimum number of characters for this string is: `1`

**pattern**: the string must match the following regular expression:&#x20;

```regexp
^[a-zA-Z][-a-zA-Z0-9]*$
```

[try pattern](https://regexr.com/?expression=%5E%5Ba-zA-Z%5D%5B-a-zA-Z0-9%5D*%24 "try regular expression with regexr.com")
