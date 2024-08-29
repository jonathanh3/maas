# MAAS

This is just my notes for setting up MAAS for testing. This is not used in production.

## Install

```
# Set enviroment variables
source .env

# Install
bash install
```

## Uploading custom images to MAAAS

TGZ image

```shell
maas admin boot-resources create \
    name='custom/ubuntu-tgz' \
    title='Ubuntu Custom TGZ' \
    architecture='amd64/generic' \
    filetype='tgz' \
    content@=custom-cloudimg.tar.gz
```

LVM raw image

```shell
maas admin boot-resources create \
    name='custom/ubuntu-raw' \
    title='Ubuntu Custom RAW' \
    architecture='amd64/generic' \
    filetype='ddgz' \
    content@=custom-ubuntu-lvm.dd.gz
```
