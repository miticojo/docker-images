## OC-CLIENT Image
[![Docker Repository on Quay](https://quay.io/repository/gcrivell/oc-client/status "Docker Repository on Quay")](https://quay.io/repository/gcrivell/oc-client)

This is a base RHEL 7 image with **oc** client (latest community version) inside.
Useful for any job/cronjob  on openshift ...

**Import into Openshift**
```
oc import-image oc-client --from=quay.io/gcrivell/oc-client --confirm
```

