# Url of the ACME server Schema

```txt
http://schema.nethserver.org/traefik/get-acme-eserver-output.json#/properties/url
```



| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                    |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [get-acme-eserver-output.json\*](traefik/get-acme-eserver-output.json "open original schema") |

## url Type

`string` ([Url of the ACME server](get-acme-eserver-output-properties-url-of-the-acme-server.md))

## url Constraints

**URI**: the string must be a URI, according to [RFC 3986](https://tools.ietf.org/html/rfc3986 "check the specification")

## url Examples

```json
"https://acme-staging-v02.api.letsencrypt.org/directory"
```
