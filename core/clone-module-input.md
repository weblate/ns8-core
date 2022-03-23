# clone-module input Schema

```txt
http://schema.nethserver.org/module/clone-module-input.json
```

Clone the module state received from rsync

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                       |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [clone-module-input.json](module/clone-module-input.json "open original schema") |

## clone-module input Type

`object` ([clone-module input](clone-module-input.md))

## clone-module input Examples

```json
{
  "credentials": [
    "dokuwiki1",
    "s3cr3t"
  ],
  "environment": {
    "IMAGE_URL": "ghcr.io/nethserver/dokuwiki:latest",
    "MODULE_UUID": "f5d24fcd-819c-4b1d-98ad-a1b2ebcee8cf",
    "DOKUWIKI_IMAGE": "docker.io/bitnami/dokuwiki:20200729.0.0-debian-10-r299",
    "DOKUWIKI_WIKI_NAME": "mywiki",
    "DOKUWIKI_USERNAME": "admin",
    "DOKUWIKI_PASSWORD": "pass",
    "DOKUWIKI_EMAIL": "davidep@nethesis.it",
    "DOKUWIKI_FULL_NAME": "Wiki Admin",
    "PHP_ENABLE_OPCACHE": "1",
    "PHP_MEMORY_LIMIT": "512M",
    "TRAEFIK_HOST": "mywiki.dp.nethserver.net",
    "TRAEFIK_HTTP2HTTPS": "False",
    "TRAEFIK_LETS_ENCRYPT": "False"
  },
  "port": 20027,
  "volumes": [
    "dokuwiki-data"
  ],
  "replace": false
}
```

# clone-module input Properties

| Property                    | Type      | Required | Nullable       | Defined by                                                                                                                                                                                   |
| :-------------------------- | :-------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [volumes](#volumes)         | `array`   | Required | cannot be null | [clone-module input](clone-module-input-properties-initial-volume-set-where-the-module-state-is-stored.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/volumes") |
| [port](#port)               | `integer` | Required | cannot be null | [clone-module input](clone-module-input-properties-rsyncd-tcp-port-number.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/port")                                 |
| [environment](#environment) | `object`  | Required | cannot be null | [clone-module input](clone-module-input-properties-environment-backup.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/environment")                              |
| [credentials](#credentials) | `array`   | Required | cannot be null | [clone-module input](clone-module-input-properties-rsyncd-service-credentials.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/credentials")                      |
| [replace](#replace)         | `boolean` | Required | cannot be null | [clone-module input](clone-module-input-properties-replace-flag.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/replace")                                        |

## volumes



`volumes`

*   is required

*   Type: `string[]` ([Name of the volume element](clone-module-input-properties-initial-volume-set-where-the-module-state-is-stored-name-of-the-volume-element.md))

*   cannot be null

*   defined in: [clone-module input](clone-module-input-properties-initial-volume-set-where-the-module-state-is-stored.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/volumes")

### volumes Type

`string[]` ([Name of the volume element](clone-module-input-properties-initial-volume-set-where-the-module-state-is-stored-name-of-the-volume-element.md))

## port



`port`

*   is required

*   Type: `integer` ([Rsyncd TCP port number](clone-module-input-properties-rsyncd-tcp-port-number.md))

*   cannot be null

*   defined in: [clone-module input](clone-module-input-properties-rsyncd-tcp-port-number.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/port")

### port Type

`integer` ([Rsyncd TCP port number](clone-module-input-properties-rsyncd-tcp-port-number.md))

### port Constraints

**minimum**: the value of this number must greater than or equal to: `1`

## environment

Copy of the environment of the original module

`environment`

*   is required

*   Type: `object` ([Environment backup](clone-module-input-properties-environment-backup.md))

*   cannot be null

*   defined in: [clone-module input](clone-module-input-properties-environment-backup.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/environment")

### environment Type

`object` ([Environment backup](clone-module-input-properties-environment-backup.md))

## credentials

An array with two elements: username, password

`credentials`

*   is required

*   Type: `string[]`

*   cannot be null

*   defined in: [clone-module input](clone-module-input-properties-rsyncd-service-credentials.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/credentials")

### credentials Type

`string[]`

### credentials Constraints

**maximum number of items**: the maximum number of items for this array is: `2`

**minimum number of items**: the minimum number of items for this array is: `2`

## replace

If set to true the original module will be erased

`replace`

*   is required

*   Type: `boolean` ([Replace flag](clone-module-input-properties-replace-flag.md))

*   cannot be null

*   defined in: [clone-module input](clone-module-input-properties-replace-flag.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/replace")

### replace Type

`boolean` ([Replace flag](clone-module-input-properties-replace-flag.md))
