# comtrya-dotfiles

## Description

This repos was created to describe how to use comtrya tool with a newly added linux machine used for VScode setup for remote plugin. 

Comtrya is a kind od a configuration management tool tha serves for bootstraping a linux OS. 

## Start with comtrya
### installing comtrya
```bash
sudo su - 
curl -fsSL https://get.comtrya.dev | sh
```

On Ubuntu 22.04 OS I do ussually get an error related to lob.ssl.so :
```bash
comtrya: error while loading shared libraries: libssl.so.1.1: cannot open shared object file: No such file or directory
```

To fix the error you need to run: 
```bash
wget http://nz2.archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2.19_amd64.deb

sudo dpkg -i libssl1.1_1.1.1f-1ubuntu2.19_amd64.deb
```

## Apply manifests: 
```bash
comtrya -d https://github.com/kravetsd/comtrya-dotfiles apply
```

