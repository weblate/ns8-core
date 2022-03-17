# set-routes input Schema

```txt
http://schema.nethserver.org/samba/set-routes-input.json
```

Decide if DC traffic is routed through the cluster VPN

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                  |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [set-routes-input.json](samba/set-routes-input.json "open original schema") |

## set-routes input Type

`object` ([set-routes input](set-routes-input.md))

## set-routes input Examples

```json
{
  "use_cluster_vpn": true,
  "realm": "AD.EXAMPLE.COM",
  "ipaddress": "10.15.21.100"
}
```

# set-routes input Properties

| Property                              | Type      | Required | Nullable       | Defined by                                                                                                                                                |
| :------------------------------------ | :-------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [use\_cluster\_vpn](#use_cluster_vpn) | `boolean` | Required | cannot be null | [set-routes input](set-routes-input-properties-use_cluster_vpn.md "http://schema.nethserver.org/samba/set-routes-input.json#/properties/use_cluster_vpn") |
| [ipaddress](#ipaddress)               | `string`  | Optional | cannot be null | [set-routes input](set-routes-input-properties-ipaddress.md "http://schema.nethserver.org/samba/set-routes-input.json#/properties/ipaddress")             |
| [realm](#realm)                       | `string`  | Optional | cannot be null | [set-routes input](set-routes-input-properties-domain-name.md "http://schema.nethserver.org/samba/set-routes-input.json#/properties/realm")               |

## use\_cluster\_vpn



`use_cluster_vpn`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [set-routes input](set-routes-input-properties-use_cluster_vpn.md "http://schema.nethserver.org/samba/set-routes-input.json#/properties/use_cluster_vpn")

### use\_cluster\_vpn Type

`boolean`

## ipaddress



`ipaddress`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [set-routes input](set-routes-input-properties-ipaddress.md "http://schema.nethserver.org/samba/set-routes-input.json#/properties/ipaddress")

### ipaddress Type

`string`

### ipaddress Constraints

**IPv4**: the string must be an IPv4 address (dotted quad), according to [RFC 2673, section 3.2](https://tools.ietf.org/html/rfc2673 "check the specification")

## realm



`realm`

*   is optional

*   Type: `string` ([Domain name](set-routes-input-properties-domain-name.md))

*   cannot be null

*   defined in: [set-routes input](set-routes-input-properties-domain-name.md "http://schema.nethserver.org/samba/set-routes-input.json#/properties/realm")

### realm Type

`string` ([Domain name](set-routes-input-properties-domain-name.md))

### realm Constraints

**maximum length**: the maximum number of characters for this string is: `140`

**minimum length**: the minimum number of characters for this string is: `1`

**pattern**: the string must match the following regular expression:&#x20;

```regexp
^[a-zA-Z][-a-zA-Z0-9]{0,62}(\.[a-zA-Z][-a-zA-Z0-9]{0,62})+$
```

[try pattern](https://regexr.com/?expression=%5E%5Ba-zA-Z%5D%5B-a-zA-Z0-9%5D%7B0%2C62%7D\(%5C.%5Ba-zA-Z%5D%5B-a-zA-Z0-9%5D%7B0%2C62%7D\)%2B%24 "try regular expression with regexr.com")
