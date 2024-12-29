# mini_zero_28
This is the procedure for building the Linux SDK for mini_zero_28.
We are currently checking whether we can release the Linux SDK.

# Prerequisites
- Ubuntu version
  - ubuntu-16.04.7-desktop-amd64.iso
  - ubuntu-16.04.7-server-amd64.iso
 
# Preparing the build machine
- necessary libraries
```
sudo apt-get install libnspr4 libnspr4-dev libncurses5-dev lib32ncurses5 lib32z1 lib32z1 git git-core openssh-server lib32stdc++6 libc6-i386 libxml2-utils bison curl lib32stdc++6 vim gawk u-boot-tools u-boot-tools:i386 libx11-dev:i386 libreadline6-dev:i386 libgl1-mesa-dev libnspr4 libnspr4-dev g++-multilib git flex bison gperf build-essential libncurses5-dev:i386 tofrodos python-markdown libxml2-utils xsltproc zlib1g-dev:i386 dpkg-dev libsdl1.2-dev libesd0-dev git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache libgl1-mesa-dev libxml2-utils xsltproc unzip m4
```

# Build Steps
1. Get archives
```
cat mplus_a133_tina_v1.0.tar.gz.* > mplus_a133_tina_v1.0.tar.gz
```

2. Check MD5 before untar
```
957e9383dbfd7bcae98a4766bc1011bd  mplus_a133_tina_v1.0.tar.gz
```

3. Untar
```
tar -xvf mplus_a133_tina_v1.0.tar.gz
```

4. Build img
```
cd lichee
source build/envsetup.sh
lunch
    [ pick --> 2. a133_aw3-tina ]
make -j8
pack
```
