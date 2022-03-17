# set-certificate input Schema

```txt
http://schema.nethserver.org/traefik/set-certificate-input.json
```

Request a let's encrypt certificate

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                              |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [set-certificate-input.json](traefik/set-certificate-input.json "open original schema") |

## set-certificate input Type

`object` ([set-certificate input](set-certificate-input.md))

## set-certificate input Examples

```json
{
  "fqdn": "example.com"
}
```

# set-certificate input Properties

| Property      | Type     | Required | Nullable       | Defined by                                                                                                                                                                    |
| :------------ | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [fqdn](#fqdn) | `string` | Required | cannot be null | [set-certificate input](set-certificate-input-properties-a-fully-qualified-domain-name.md "http://schema.nethserver.org/traefik/set-certificate-input.json#/properties/fqdn") |

## fqdn



`fqdn`

*   is required

*   Type: `string` ([A fully qualified domain name](set-certificate-input-properties-a-fully-qualified-domain-name.md))

*   cannot be null

*   defined in: [set-certificate input](set-certificate-input-properties-a-fully-qualified-domain-name.md "http://schema.nethserver.org/traefik/set-certificate-input.json#/properties/fqdn")

### fqdn Type

`string` ([A fully qualified domain name](set-certificate-input-properties-a-fully-qualified-domain-name.md))

### fqdn Constraints

**hostname**: the string must be a hostname, according to [RFC 1123, section 2.1](https://tools.ietf.org/html/rfc1123 "check the specification")
