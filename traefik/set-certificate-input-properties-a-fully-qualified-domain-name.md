# A fully qualified domain name Schema

```txt
http://schema.nethserver.org/traefik/set-certificate-input.json#/properties/fqdn
```



| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [set-certificate-input.json\*](traefik/set-certificate-input.json "open original schema") |

## fqdn Type

`string` ([A fully qualified domain name](set-certificate-input-properties-a-fully-qualified-domain-name.md))

## fqdn Constraints

**hostname**: the string must be a hostname, according to [RFC 1123, section 2.1](https://tools.ietf.org/html/rfc1123 "check the specification")
