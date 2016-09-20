# config for generic-amd64

## Prerequisites
- ubuntu-recovery-image: could be install from http://github.com/Lyoncore/ubuntu-recovery-image
- ubuntu-image: could be install via:
``` bash
sudo snap install --edge --devmode ubuntu-image
```

## build base image
```
sh cook-image.sh
```

## build recovery binary
``` bash
git clone https://github.com/Lyoncore/generic-amd64-config.git
cd generic-amd64-config/
go get launchpad.net/godeps
godeps -t -u dependencies.tsv
go run build.go build
```

## generate image with ubuntu-recovery-image
``` bash
ubuntu-recovery-image
```
