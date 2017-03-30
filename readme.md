# BIW Rancher Catalog

Also refer to the [Rancher documentation](https://docs.rancher.com/rancher/v1.5/en/catalog/private-catalog/).

### BIW Categories

The `Category` attribute in the `config.yml` is free-form but we're trying to keep our setup to these options:

- Development

- Communications

- CI / CD

- Metrics / Monitoring

- Administration


### Standard Setup

To try and simplify this and make it a bit more consistent across catalog items the below standard setup helps identify where values should be reused across the required files.

###### `config.yml`

```yaml
name: <app name>
description: |
  <app description>
version: <latest version code>
category: <category>
```

###### `catalogIcon-<app name>.svg`

Can be whatever you want :)

###### `<version index>/readme.md`

brief description about the catalog item and what it does.  good idea to call out what's different about this version (if it's something after the first version).

###### `<version index>/docker-compose.yml`

Just the docker-compose that the catalog item needs.

###### `<version index>/rancher-compose.yml`

The `.catalog` section at the top is below, everything after that is just whatever what catalog item needs.

```yaml
.catalog:
  name: <app name>
  version: <version code>
  uuid: <app name lowercased and hyphenated>
  description: |
    <app description in markdown>
...
the rest of your config
...
```