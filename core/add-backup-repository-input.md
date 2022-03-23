# add-backup-repository input Schema

```txt
http://schema.nethserver.org/cluster/add-backup-repository-input.json
```

Input schema of the add-backup-repository action

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                          |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [add-backup-repository-input.json](cluster/add-backup-repository-input.json "open original schema") |

## add-backup-repository input Type

`object` ([add-backup-repository input](add-backup-repository-input.md))

any of

*   all of

    *   [BackBlaze schema](add-backup-repository-input-anyof-0-allof-backblaze-schema.md "check type definition")

*   all of

    *   [S3-based provider schema](add-backup-repository-input-anyof-1-allof-s3-based-provider-schema.md "check type definition")

## add-backup-repository input Examples

```json
{
  "name": "repository1",
  "provider": "backblaze",
  "url": "b2:mybucket/mybackup",
  "password": "",
  "parameters": {
    "b2_account_id": "YEFYEIOEHGO",
    "b2_account_key": "sdifjsiodv7sdv7suivyhsfv7fvyhdfvb7d"
  }
}
```

```json
{
  "name": "repository2",
  "provider": "aws",
  "url": "s3:s3.amazonaws.com/mybucket/mybackup",
  "password": "45a1905ef8de3c03b05d47071754bd5ddbfec0edaa56d4c44f981386f3f24888",
  "parameters": {
    "aws_default_region": "us-east-1",
    "aws_access_key_id": "IEIEEHEHEW",
    "aws_secret_access_key": "edfjksof798r7fsdfiougvf7df"
  }
}
```

```json
{
  "name": "repository 3",
  "provider": "digitalocean",
  "password": "",
  "url": "s3:ams3.digitaloceanspaces.com/mybucket/mybackup",
  "parameters": {
    "aws_access_key_id": "XJEMERNGRIWGN",
    "aws_secret_access_key": "897wergjkegher987geriugheruiger789"
  }
}
```

# add-backup-repository input Properties

| Property                  | Type     | Required | Nullable       | Defined by                                                                                                                                                                                    |
| :------------------------ | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [provider](#provider)     | `string` | Required | cannot be null | [add-backup-repository input](add-backup-repository-input-properties-repository-provider.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/properties/provider")     |
| [name](#name)             | `string` | Required | cannot be null | [add-backup-repository input](add-backup-repository-input-properties-backup-repository-name.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/properties/name")      |
| [url](#url)               | `string` | Required | cannot be null | [add-backup-repository input](add-backup-repository-input-properties-restic-url.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/properties/url")                   |
| [password](#password)     | `string` | Required | cannot be null | [add-backup-repository input](add-backup-repository-input-properties-encryption-token.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/properties/password")        |
| [parameters](#parameters) | `object` | Required | cannot be null | [add-backup-repository input](add-backup-repository-input-properties-connection-parameters.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/properties/parameters") |

## provider



`provider`

*   is required

*   Type: `string` ([Repository provider](add-backup-repository-input-properties-repository-provider.md))

*   cannot be null

*   defined in: [add-backup-repository input](add-backup-repository-input-properties-repository-provider.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/properties/provider")

### provider Type

`string` ([Repository provider](add-backup-repository-input-properties-repository-provider.md))

### provider Constraints

**minimum length**: the minimum number of characters for this string is: `1`

## name



`name`

*   is required

*   Type: `string` ([Backup repository name](add-backup-repository-input-properties-backup-repository-name.md))

*   cannot be null

*   defined in: [add-backup-repository input](add-backup-repository-input-properties-backup-repository-name.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/properties/name")

### name Type

`string` ([Backup repository name](add-backup-repository-input-properties-backup-repository-name.md))

## url

URL of the repository in restic format. Must be unique.

`url`

*   is required

*   Type: `string` ([Restic URL](add-backup-repository-input-properties-restic-url.md))

*   cannot be null

*   defined in: [add-backup-repository input](add-backup-repository-input-properties-restic-url.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/properties/url")

### url Type

`string` ([Restic URL](add-backup-repository-input-properties-restic-url.md))

## password

Select the password for restic encryption. If this is empty the API will generate a random password

`password`

*   is required

*   Type: `string` ([Encryption token](add-backup-repository-input-properties-encryption-token.md))

*   cannot be null

*   defined in: [add-backup-repository input](add-backup-repository-input-properties-encryption-token.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/properties/password")

### password Type

`string` ([Encryption token](add-backup-repository-input-properties-encryption-token.md))

## parameters



`parameters`

*   is required

*   Type: `object` ([Connection parameters](add-backup-repository-input-properties-connection-parameters.md))

*   cannot be null

*   defined in: [add-backup-repository input](add-backup-repository-input-properties-connection-parameters.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/properties/parameters")

### parameters Type

`object` ([Connection parameters](add-backup-repository-input-properties-connection-parameters.md))

# add-backup-repository input Definitions

## Definitions group b2\_parameters

Reference this group by using

```json
{"$ref":"http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/b2_parameters"}
```

| Property                            | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                           |
| :---------------------------------- | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [b2\_account\_id](#b2_account_id)   | `string` | Required | cannot be null | [add-backup-repository input](add-backup-repository-input-defs-b2-backblaze-protocol-parameters-properties-b2_account_id.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/b2_parameters/properties/b2_account_id")   |
| [b2\_account\_key](#b2_account_key) | `string` | Required | cannot be null | [add-backup-repository input](add-backup-repository-input-defs-b2-backblaze-protocol-parameters-properties-b2_account_key.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/b2_parameters/properties/b2_account_key") |

### b2\_account\_id



`b2_account_id`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [add-backup-repository input](add-backup-repository-input-defs-b2-backblaze-protocol-parameters-properties-b2_account_id.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/b2_parameters/properties/b2_account_id")

#### b2\_account\_id Type

`string`

### b2\_account\_key



`b2_account_key`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [add-backup-repository input](add-backup-repository-input-defs-b2-backblaze-protocol-parameters-properties-b2_account_key.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/b2_parameters/properties/b2_account_key")

#### b2\_account\_key Type

`string`

## Definitions group s3\_parameters

Reference this group by using

```json
{"$ref":"http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/s3_parameters"}
```

| Property                                           | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                          |
| :------------------------------------------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [aws\_default\_region](#aws_default_region)        | `string` | Optional | cannot be null | [add-backup-repository input](add-backup-repository-input-defs-s3-amazon-aws-protocol-parameters-properties-aws_default_region.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/s3_parameters/properties/aws_default_region")       |
| [aws\_access\_key\_id](#aws_access_key_id)         | `string` | Required | cannot be null | [add-backup-repository input](add-backup-repository-input-defs-s3-amazon-aws-protocol-parameters-properties-aws_access_key_id.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/s3_parameters/properties/aws_access_key_id")         |
| [aws\_secret\_access\_key](#aws_secret_access_key) | `string` | Required | cannot be null | [add-backup-repository input](add-backup-repository-input-defs-s3-amazon-aws-protocol-parameters-properties-aws_secret_access_key.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/s3_parameters/properties/aws_secret_access_key") |

### aws\_default\_region



`aws_default_region`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [add-backup-repository input](add-backup-repository-input-defs-s3-amazon-aws-protocol-parameters-properties-aws_default_region.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/s3_parameters/properties/aws_default_region")

#### aws\_default\_region Type

`string`

### aws\_access\_key\_id



`aws_access_key_id`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [add-backup-repository input](add-backup-repository-input-defs-s3-amazon-aws-protocol-parameters-properties-aws_access_key_id.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/s3_parameters/properties/aws_access_key_id")

#### aws\_access\_key\_id Type

`string`

### aws\_secret\_access\_key



`aws_secret_access_key`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [add-backup-repository input](add-backup-repository-input-defs-s3-amazon-aws-protocol-parameters-properties-aws_secret_access_key.md "http://schema.nethserver.org/cluster/add-backup-repository-input.json#/$defs/s3_parameters/properties/aws_secret_access_key")

#### aws\_secret\_access\_key Type

`string`
