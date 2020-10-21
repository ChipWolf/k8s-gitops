# Light-weight mixed-architecture cluster setup with k3s

## installation (one-time actions)

### k3s node installation

See [k3s bootstrapping](https://github.com/billimek/homelab-infrastructure/tree/master/k3s) for details on creating the k3s cluster itself

```shell
./bootstrap-cluster.sh
```

This [script](bootstrap-cluster.sh) does several things:

1. Installs flux
2. Retrieves the new flux public key and saves it to the GitHub repo as a repo key (see [add-repo-key.sh](add-repo-key.sh))

### backup & restore

`velero` is used as the backup mechanism.  However, as an alternative for situations where it is, unfortunately, necessary to backup & restore a persistent volume (e.g. completely removing a chart that leverages a persistent volume), the [`backup.sh`](backup.sh) and [`restore.sh`](restore.sh) scripts may be used.  Examine the scripts to learn more.
