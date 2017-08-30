Terraform Provider for Outscale (unofficial)
==================

Requirements
------------

-   [Terraform](https://www.terraform.io/downloads.html) 0.9.11 
-   [Go](https://golang.org/doc/install) 1.8 (to build the provider plugin)

Install
---------------------

Download the binary and put it in the same folder than terraform binary

```
$ wget https://github.com/remijouannet/terraform-provider-osc/releases/download/v0.1/terraform-provider-osc_darwin_amd64_v0.1.zip
$ unzip terraform-provider-osc_darwin_amd64_v0.1.zip
$ cp terraform-provider-osc_darwin_amd64_v0.1/terraform-provider-osc_v0.1.zip $(dirname $(which terraform))
$ chmod +x $(dirname $(which terraform))/terraform-provider-osc_darwin_amd64_v0.1
```


Build without docker
---------------------

Clone repository to: `$GOPATH/src/github.com/remijouannet/terraform-provider-osc`

```
$ mkdir -p $GOPATH/src/github.com/remijouannet; cd $GOPATH/src/github.com/remijouannet
$ git clone git@github.com:remijouannet/terraform-provider-osc
```

Enter the provider directory and build the provider

```
$ cd $GOPATH/src/github.com/remijouannet/terraform-provider-osc
$ make build
```

Build with docker
---------------------

build the docker image

```
$ make docker-image
```

build the binaries, you'll find all the binaries in pkg/

```
$ make docker-build
```
