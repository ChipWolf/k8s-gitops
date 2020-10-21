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
