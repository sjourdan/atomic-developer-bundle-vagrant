# Atomic ADB Vagrant

The [Atomic Developer Bundle (ADB)](https://github.com/projectatomic/adb-atomic-developer-bundle) is a prepackaged development environment filled with production-grade pre-configured tools that makes container developer's lives easier. The ADB supports the development of multi-container applications against different technologies and orchestrators while providing a path that promotes best practices.

## Vagrant ADB Plugin

    vagrant plugin install vagrant-adbinfo

## Launch ADB 

    vagrant up --provider=virtualbox

Grab some information: 

```
vagrant adbinfo
# Set the following environment variables to enable access to the
# docker daemon running inside of the vagrant virtual machine:

export DOCKER_HOST=tcp://172.28.128.3:2376
export DOCKER_CERT_PATH=/Users/sjourdan/dev/git/atomic-developer-bundle-vagrant/.vagrant/machines/default/virtualbox/.docker
export DOCKER_TLS_VERIFY=1
export DOCKER_MACHINE_NAME=ef3abbd

# run following command to configure your shell:
# eval "$(vagrant adbinfo)"
```

*Warning*: you need a compatible Docker version or you'll get an error.

## Usage

### Docker

    docker ps

