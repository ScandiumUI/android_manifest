# ScandiumUI Manifest

<p align="center">
  <b>ScandiumUI</b><br>
  <i>Settings • Setup Wizard • Quick Settings • SystemUI — reimagined.</i>
</p>

---

## Getting Started

### Prerequisites

- **OS**: Ubuntu 20.04+ / 22.04+ (64-bit)
- **RAM**: Minimal 32GB (64GB disarankan)
- **Storage**: Minimal 400GB SSD
- **Tools**: Git, Repo, Python 3, OpenJDK 21

### Install Dependencies (Ubuntu)

```bash
sudo apt update
sudo apt install -y bc bison build-essential ccache curl flex g++-multilib \
  gcc-multilib git git-lfs gnupg gperf imagemagick lib32readline-dev \
  lib32z1-dev libelf-dev liblz4-tool libsdl1.2-dev libssl-dev \
  libxml2 libxml2-utils lzop pngcrush rsync schedtool squashfs-tools \
  xsltproc zip zlib1g-dev python3 python-is-python3 openjdk-21-jdk
```

### Initialize Repository

```bash
mkdir -p ~/scandiumui && cd ~/scandiumui
repo init -u https://github.com/ScandiumUI/android_manifest.git -b sixteen-qpr2 --git-lfs
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build

```bash
source build/envsetup.sh
breakfast <devicecodename>
m scandium
```

## License

Copyright (C) 2026 ScandiumUI

Licensed under the Apache License, Version 2.0.
