# rocky-linux-9.*
Create a Docker container base image using Rocky Linux version 9.6 tar file

Step1: Load in your system, container tar file
Source: https://download.rockylinux.org/pub/rocky/9.6/images/x86_64/

```bash
# For 9.6
wget https://dl.rockylinux.org/vault/rocky/9.6/images/x86_64/Rocky-9-Container-Base-9.6-20250531.0.x86_64.tar.xz

# For 9.4
wget https://dl.rockylinux.org/vault/rocky/9.4/images/x86_64/Rocky-9-Container-Base-9.4-20240523.0.x86_64.tar.xz

#For 9.2
wget https://dl.rockylinux.org/vault/rocky/9.2/images/x86_64/Rocky-9-Container-Base-9.2-20230513.0.x86_64.tar.xz
```

Step2: extract  the xz  file (example 9.6)

```bash
xz -d Rocky-9-Container-Base-9.6-20250531.0.x86_64.tar.xz
```

Step3: Create docker image

```bash
docker import Rocky-9-Container-Base-9.6-20250531.0.x86_64.tar rockylinux9:9.6
```
