# get-acme-server output Schema

```txt
http://schema.nethserver.org/traefik/get-acme-eserver-output.json
```

Get the URL of the ACME server

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                  |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [get-acme-eserver-output.json](traefik/get-acme-eserver-output.json "open original schema") |

## get-acme-server output Type

`object` ([get-acme-server output](get-acme-eserver-output.md))

## get-acme-server output Examples

```json
{
  "url": "https://acme-staging-v02.api.letsencrypt.org/directory"
}
```

# get-acme-server output Properties

| Property    | Type     | Required | Nullable       | Defined by                                                                                                                                                                 |
| :---------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [url](#url) | `string` | Required | cannot be null | [get-acme-server output](get-acme-eserver-output-properties-url-of-the-acme-server.md "http://schema.nethserver.org/traefik/get-acme-eserver-output.json#/properties/url") |

## url



`url`

*   is required

*   Type: `string` ([Url of the ACME server](get-acme-eserver-output-properties-url-of-the-acme-server.md))

*   cannot be null

*   defined in: [get-acme-server output](get-acme-eserver-output-properties-url-of-the-acme-server.md "http://schema.nethserver.org/traefik/get-acme-eserver-output.json#/properties/url")

### url Type

`string` ([Url of the ACME server](get-acme-eserver-output-properties-url-of-the-acme-server.md))

### url Constraints

**URI**: the string must be a URI, according to [RFC 3986](https://tools.ietf.org/html/rfc3986 "check the specification")

### url Examples

```json
"https://acme-staging-v02.api.letsencrypt.org/directory"
```
