# Environment backup Schema

```txt
http://schema.nethserver.org/module/clone-module-input.json#/properties/environment
```

Copy of the environment of the original module

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                         |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [clone-module-input.json\*](module/clone-module-input.json "open original schema") |

## environment Type

`object` ([Environment backup](clone-module-input-properties-environment-backup.md))

# environment Properties

| Property                 | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                    |
| :----------------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [IMAGE\_URL](#image_url) | `string` | Optional | cannot be null | [clone-module input](clone-module-input-properties-environment-backup-properties-image_url.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/environment/properties/IMAGE_URL")     |
| `^[^=]+$`                | `string` | Optional | cannot be null | [clone-module input](clone-module-input-properties-environment-backup-patternproperties-.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/environment/patternProperties/^\[^=]+$") |

## IMAGE\_URL

URL of the module root image

`IMAGE_URL`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [clone-module input](clone-module-input-properties-environment-backup-properties-image_url.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/environment/properties/IMAGE_URL")

### IMAGE\_URL Type

`string`

### IMAGE\_URL Constraints

**minimum length**: the minimum number of characters for this string is: `1`

### IMAGE\_URL Examples

```json
"ghcr.io/nethserver/mymodule:v2.3.2"
```

## Pattern: `^[^=]+$`



`^[^=]+$`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [clone-module input](clone-module-input-properties-environment-backup-patternproperties-.md "http://schema.nethserver.org/module/clone-module-input.json#/properties/environment/patternProperties/^\[^=]+$")

### ^\[^=]+$ Type

`string`
