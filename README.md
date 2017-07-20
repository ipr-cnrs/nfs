# NFS

1. [Overview](#overview)
2. [Role Variables](#role-variables)
     * [OS Specific Variables](#os-specific-variables)
3. [Example Playbook](#example-playbook)
4. [Configuration](#configuration)
5. [Development](#development)
5. [License](#license)
6. [Author Information](#author-information)

## Overview

Manage NFS.

## Role Variables

### OS Specific Variables

Please see default value by Operating System file in [vars][vars directory] directory.

## Example Playbook

* Use defaults vars :

``` yml
- hosts: serverXYZ
  roles:
    - role: ipr-cnrs.nfs
```

## Configuration

This role will :
* Install needed packages to provide `nfs-client`.

## Development

This source code comes from our [Gogs instance][nfs source] and the [Github repo][nfs github] exist just to be able to send the role to Ansible Galaxy…

But feel free to send issue/PR here :)

Thanks to this [hook][gogs to github hook], Github automatically got updates from our [Gogs instance][nfs source] :)

## License

[WTFPL][wtfpl website]

## Author Information

Jérémy Gardais
* Source : [on IPR's Gogs][nfs source]
* [IPR][ipr website] (Institut de Physique de Rennes)

[vars directory]: ./vars
[gogs to github hook]: https://stackoverflow.com/a/21998477
[nfs source]: https://git.ipr.univ-rennes1.fr/cellinfo/ansible.nfs
[nfs github]: https://github.com/ipr-cnrs/nfs
[wtfpl website]: http://www.wtfpl.net/about/
[ipr website]: https://ipr.univ-rennes1.fr/
