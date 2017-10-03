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

This role manages NFS client installation and configuration using fixed ports.

## Role Variables

* **nfs_cli_manage** : If `nfs-client` should be managed with this role [default : `true`].
* **nfs_cli_pkg_state** : State of new `nfs-client` package(s) [default : `installed`].
* **nfs_cli_conf_path** : Configuration file for `nfs-client` [default : `/etc/default/nfs-common`].
* **nfs_cli_conf_tpl** : Template used to generate the previous config file [default : `etc/default/nfs-common.j2`].
* **nfs_quota_conf_path** : Configuration file for `quota` (`nfs-client`) [default : `/etc/default/quota`].
* **nfs_quota_conf_tpl** : Template used to generate the previous config file [default : `etc/default/quota.j2`].
* **nfs_rpc_nfsd** : Port used by the NFS server [default : `2049`].
* **nfs_rpc_nfs_cb** : Port used by RPC callback [default : `32764`].
* **nfs_rpc_statd_bc** : Port used by RPC statd broadcast [default : `32765`].
* **nfs_rpc_statd** : Port used by RPC statd listener [default : `32766`].
* **nfs_rpc_mountd** : Port used by RPC mountd [default : `32767`].
* **nfs_rpc_lockd** : Port used by RPC nlock manager [default : `32768`].
* **nfs_rpc_quotad** : Port used by RPC quotad [default : `32769`].

### OS Specific Variables

Please see default value by Operating System file in [vars][vars directory] directory.

* **nfs_cli_pkg_list** : The list of packages to install to provide `nfs-client`.

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
* Manage `nfs-client` configuration files.
* Fix rpcbind ports.

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
