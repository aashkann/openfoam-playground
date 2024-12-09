---
sidebar_position: 0
---


# Install OpenFOAM 12 on Ubuntu

OpenFOAM 12 marks a significant new release, distributed through the openfoam12 package. It is paired with ParaView, utilizing the standard paraview package for Ubuntu versions 24.04 and 22.04, and a customized paraviewopenfoam510 package for Ubuntu 20.04. OpenFOAM 12 is compatible with the following Ubuntu versions:

#### Supported Ubuntu Versions
- Ubuntu 20.04 LTS (focal)
- Ubuntu 22.04 LTS (jammy)
- Ubuntu 24.04 LTS (noble)

#### Installation Steps

```bash
# 1. Add OpenFOAM Repository
sudo sh -c "wget -O - https://dl.openfoam.org/gpg.key > /etc/apt/trusted.gpg.d/openfoam.asc"
sudo add-apt-repository http://dl.openfoam.org/ubuntu

# Note: The above step only needs to be done once per system.

# 2. Update Package List
sudo apt update

# 3. Install OpenFOAM 12
sudo apt -y install openfoam12

# Note: For Ubuntu 20.04, this will also install ParaView or a custom ParaView package.


# This will also install ParaView or a custom ParaView package (for Ubuntu 20.04).
```
#### Patching OpenFOAM 12

Update all packages including OpenFOAM
```bash
sudo apt update
sudo apt upgrade

# Or update only OpenFOAM 12
sudo apt update
sudo apt install --only-upgrade openfoam12
```

[Source](https://openfoam.org/download/12-ubuntu/)
