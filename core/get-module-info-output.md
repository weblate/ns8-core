# get-module-info output Schema

```txt
http://schema.nethserver.org/cluster/get-module-info-output.json
```

Get module info output

| Abstract               | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                |
| :--------------------- | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------------------------------------- |
| Cannot be instantiated | Yes        | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [get-module-info-output.json](cluster/get-module-info-output.json "open original schema") |

## get-module-info output Type

merged type ([get-module-info output](get-module-info-output.md))

one (and only one) of

*   [Untitled null in get-module-info output](get-module-info-output-oneof-0.md "check type definition")

*   [Untitled object in get-module-info output](get-module-info-output-definitions-module.md "check type definition")

## get-module-info output Examples

```json
{
  "name": "dokuwiki",
  "description": {
    "en": "Auto-generated description for dokuwiki"
  },
  "logo": "http://127.0.0.1:8000/logo.png",
  "screenshots": [
    "http://127.0.0.1:8000/screenshots/template%3Adokuwiki_template.png"
  ],
  "categories": [
    "unknown"
  ],
  "authors": [
    {
      "name": "unknown",
      "email": "info@nethserver.org"
    }
  ],
  "docs": {
    "documentation_url": "https://docs.nethserver.org",
    "bug_url": "https://github.com/NethServer/dev",
    "code_url": "https://github.com/NethServer/"
  },
  "source": "ghcr.io/nethserver/dokuwiki",
  "repository": "t3"
}
```

# get-module-info output Definitions

## Definitions group module

Reference this group by using

```json
{"$ref":"http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module"}
```

| Property                                  | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                |
| :---------------------------------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [name](#name)                             | `string` | Required | cannot be null | [get-module-info output](get-module-info-output-definitions-module-properties-name.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/name")                             |
| [description](#description)               | `object` | Required | cannot be null | [get-module-info output](get-module-info-output-definitions-module-properties-description.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/description")               |
| [logo](#logo)                             | `string` | Required | can be null    | [get-module-info output](get-module-info-output-definitions-module-properties-logo.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/logo")                             |
| [categories](#categories)                 | `array`  | Required | cannot be null | [get-module-info output](get-module-info-output-definitions-module-properties-categories.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/categories")                 |
| [authors](#authors)                       | `array`  | Required | cannot be null | [get-module-info output](get-module-info-output-definitions-module-properties-authors.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/authors")                       |
| [docs](#docs)                             | `object` | Required | cannot be null | [get-module-info output](get-module-info-output-definitions-module-properties-docs.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/docs")                             |
| [source](#source)                         | `string` | Required | cannot be null | [get-module-info output](get-module-info-output-definitions-module-properties-source.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/source")                         |
| [repository](#repository)                 | `string` | Optional | cannot be null | [get-module-info output](get-module-info-output-definitions-module-properties-repository.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/repository")                 |
| [repository_updated](#repository_updated) | `string` | Optional | cannot be null | [get-module-info output](get-module-info-output-definitions-module-properties-repository_updated.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/repository_updated") |

### name

Unique name of a package

`name`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [get-module-info output](get-module-info-output-definitions-module-properties-name.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/name")

#### name Type

`string`

### description

A map of language codes (eg. en, it) with the translated description

`description`

*   is required

*   Type: `object` ([Details](get-module-info-output-definitions-module-properties-description.md))

*   cannot be null

*   defined in: [get-module-info output](get-module-info-output-definitions-module-properties-description.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/description")

#### description Type

`object` ([Details](get-module-info-output-definitions-module-properties-description.md))

### logo

The filename of the logo. The logo must be a PNG image of 256x256 pixels

`logo`

*   is required

*   Type: `string`

*   can be null

*   defined in: [get-module-info output](get-module-info-output-definitions-module-properties-logo.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/logo")

#### logo Type

`string`

### categories



`categories`

*   is required

*   Type: `string[]`

*   cannot be null

*   defined in: [get-module-info output](get-module-info-output-definitions-module-properties-categories.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/categories")

#### categories Type

`string[]`

### authors



`authors`

*   is required

*   Type: `object[]` ([Details](get-module-info-output-definitions-module-properties-authors-items.md))

*   cannot be null

*   defined in: [get-module-info output](get-module-info-output-definitions-module-properties-authors.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/authors")

#### authors Type

`object[]` ([Details](get-module-info-output-definitions-module-properties-authors-items.md))

### docs



`docs`

*   is required

*   Type: `object` ([Details](get-module-info-output-definitions-module-properties-docs.md))

*   cannot be null

*   defined in: [get-module-info output](get-module-info-output-definitions-module-properties-docs.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/docs")

#### docs Type

`object` ([Details](get-module-info-output-definitions-module-properties-docs.md))

### source

URL of package inside a container registry. The URL must not contain the prefix 'docker://' or similar

`source`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [get-module-info output](get-module-info-output-definitions-module-properties-source.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/source")

#### source Type

`string`

### repository

The internal ID of the repository inside redis

`repository`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [get-module-info output](get-module-info-output-definitions-module-properties-repository.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/repository")

#### repository Type

`string`

### repository_updated

Date and time of last modification to remote repodata

`repository_updated`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [get-module-info output](get-module-info-output-definitions-module-properties-repository_updated.md "http://schema.nethserver.org/cluster/get-module-info-output.json#/definitions/module/properties/repository_updated")

#### repository_updated Type

`string`
