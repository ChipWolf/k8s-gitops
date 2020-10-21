# kube-system namespace

## descheduler

Leveraging descheduler to automatically evict pods that no longer satisfy their NodeAffinity constraints.  This is used to work in concert with `node-feature-discovery` such that when USB devices are moved from one node to a different node, the pods requiring the USB devices will be properly forced to reschedule to the new location

## [kured](https://github.com/weaveworks/kured)

![kured](https://i.imgur.com/wYWTMGI.png)

Automatically drain and reboot nodes when a reboot is required (e.g. a kernel update was applied)

## metallb

[Run your own on-prem LoadBalancer](https://metallb.universe.tf/)

## nfs-client-provisioner

Using the [nfs-client storage type](https://github.com/kubernetes-incubator/external-storage/tree/master/nfs-client)

## nfs-pv

nfs-based persistent mounts for various pod access (media mount & data mount)

## ingress-nginx

![ingress-nginx](https://i.imgur.com/b21MHEE.png)

ingress-nginx controller leveraging cert-manager as the central cert store for the wildcard certificate
