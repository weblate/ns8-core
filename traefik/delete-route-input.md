# set-acme-server input Schema

```txt
http://schema.nethserver.org/traefik/delete-route-input.json
```

Set the URL of the ACME server

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [delete-route-input.json](traefik/delete-route-input.json "open original schema") |

## set-acme-server input Type

`object` ([set-acme-server input](delete-route-input.md))

## set-acme-server input Examples

```json
{
  "url": "https://acme-staging-v02.api.letsencrypt.org/directory"
}
```

# set-acme-server input Properties

| Property    | Type     | Required | Nullable       | Defined by                                                                                                                                                      |
| :---------- | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [url](#url) | `string` | Required | cannot be null | [set-acme-server input](delete-route-input-properties-url-of-the-acme-server.md "http://schema.nethserver.org/traefik/delete-route-input.json#/properties/url") |

## url



`url`

*   is required

*   Type: `string` ([Url of the ACME server](delete-route-input-properties-url-of-the-acme-server.md))

*   cannot be null

*   defined in: [set-acme-server input](delete-route-input-properties-url-of-the-acme-server.md "http://schema.nethserver.org/traefik/delete-route-input.json#/properties/url")

### url Type

`string` ([Url of the ACME server](delete-route-input-properties-url-of-the-acme-server.md))

### url Constraints

**URI**: the string must be a URI, according to [RFC 3986](https://tools.ietf.org/html/rfc3986 "check the specification")

### url Examples

```json
"https://acme-staging-v02.api.letsencrypt.org/directory"
```
