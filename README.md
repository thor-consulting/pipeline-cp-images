## Pipeline's Control Plane Image creation 

### List targets
```bash
make list
```

### Dry run
```bash
DRY_RUN=1 \
make build-aws-ubuntu-xenial
```

### Run with user environment
```
export AWS_REGION=eu-west-1
export AWS_DEFAULT_REGION=eu-west-1
export AWS_SSH_USERNAME=ubuntu

export AWS_SOURCE_AMI=ami-add175d4
export AWS_INTANCE_TYPE=c4.large
export AWS_SPOT_PRICE="0.02"
export AWS_ACCESS_KEY_ID=
export AWS_SECRET_ACCESS_KEY=

export KUBERNETES_RELEASE_TAG=v1.7.3
export ETCD_RELEASE_TAG=3.0.17
export K8S_DNS_RELEASE_TAG=1.14.4
export HELM_RELEASE_TAG=v2.6.0
export PROMETHEUS_RELEASE_TAG=v1.7.1

export BASE_NAME=pipeline-cp-image

make build-aws-ubuntu-xenial
```

### Supported regions

```
eu-west-1
```

## Latest Image

* eu-west-1:  `ami-1bf45662`
