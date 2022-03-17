# get-defaults output Schema

```txt
http://schema.nethserver.org/samba/get-defaults-output.json
```

Return values that suit the configure-module action input

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [get-defaults-output.json](samba/get-defaults-output.json "open original schema") |

## get-defaults output Type

`object` ([get-defaults output](get-defaults-output.md))

## get-defaults output Examples

```json
{
  "nbdomain": "AD",
  "adminuser": "administrator",
  "hostname": "dc2",
  "realm": "ad.dp.nethserver.net",
  "ipaddress_list": [
    {
      "ipaddress": "10.18.0.5",
      "label": "eth0 (enp0s3, ens3)"
    },
    {
      "ipaddress": "10.110.16.2",
      "label": "eth1 (enp0s4, ens4)"
    },
    {
      "ipaddress": "10.5.4.1",
      "label": "wg0"
    }
  ]
}
```

# get-defaults output Properties

| Property                           | Type     | Required | Nullable       | Defined by                                                                                                                                                       |
| :--------------------------------- | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [adminuser](#adminuser)            | `string` | Required | cannot be null | [get-defaults output](get-defaults-output-properties-adminuser.md "http://schema.nethserver.org/samba/get-defaults-output.json#/properties/adminuser")           |
| [hostname](#hostname)              | `string` | Required | cannot be null | [get-defaults output](get-defaults-output-properties-hostname.md "http://schema.nethserver.org/samba/get-defaults-output.json#/properties/hostname")             |
| [realm](#realm)                    | `string` | Required | cannot be null | [get-defaults output](get-defaults-output-properties-realm.md "http://schema.nethserver.org/samba/get-defaults-output.json#/properties/realm")                   |
| [nbdomain](#nbdomain)              | `string` | Required | cannot be null | [get-defaults output](get-defaults-output-properties-nbdomain.md "http://schema.nethserver.org/samba/get-defaults-output.json#/properties/nbdomain")             |
| [ipaddress\_list](#ipaddress_list) | `array`  | Required | cannot be null | [get-defaults output](get-defaults-output-properties-ipaddress_list.md "http://schema.nethserver.org/samba/get-defaults-output.json#/properties/ipaddress_list") |

## adminuser



`adminuser`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [get-defaults output](get-defaults-output-properties-adminuser.md "http://schema.nethserver.org/samba/get-defaults-output.json#/properties/adminuser")

### adminuser Type

`string`

## hostname



`hostname`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [get-defaults output](get-defaults-output-properties-hostname.md "http://schema.nethserver.org/samba/get-defaults-output.json#/properties/hostname")

### hostname Type

`string`

## realm



`realm`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [get-defaults output](get-defaults-output-properties-realm.md "http://schema.nethserver.org/samba/get-defaults-output.json#/properties/realm")

### realm Type

`string`

## nbdomain



`nbdomain`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [get-defaults output](get-defaults-output-properties-nbdomain.md "http://schema.nethserver.org/samba/get-defaults-output.json#/properties/nbdomain")

### nbdomain Type

`string`

## ipaddress\_list



`ipaddress_list`

*   is required

*   Type: `object[]` ([Details](get-defaults-output-properties-ipaddress_list-items.md))

*   cannot be null

*   defined in: [get-defaults output](get-defaults-output-properties-ipaddress_list.md "http://schema.nethserver.org/samba/get-defaults-output.json#/properties/ipaddress_list")

### ipaddress\_list Type

`object[]` ([Details](get-defaults-output-properties-ipaddress_list-items.md))
