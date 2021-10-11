<!----------------------------[ Navigation Links ]----------------------------->

[‹‹ Overview]: ../README

[Translating]: ../Translation/Overview
[Grammars]: ../Grammar/Overview
[Building]: ../Build/Overview
[Contribute]: ..Engage/Contribute

<!-------------------------------[ Navigation ]-------------------------------->

##### [‹‹ Overview]

##### 「 [Building] 」 『 [Translating] 』 『 [Grammars] 』 『 [Contribute] 』

---

<!--------------------------------[ Linux Links ]------------------------------>



<!----------------------------------[ Linux ]---------------------------------->

# Linux Build

Compiling **TeXStudio** on Linux is easy, as all required<br>
packages can be found in your package manager.

**Please Install The Dependencies Before Continuing**

##### Build methods:

- **QMake**<br>
    Use `qmake; make` to build<br>
    and `make install` to install.


- **Build Script**<br>
    Execute the `./Build.sh` build script.


- **QT Creator**<br>
    Open the `texstudio.pro` file<br>
    in **Qt Creator** and build it there.


- **Distro Compilation**<br>
    Your distribution may provide a<br>
    dedicated tool for compilation.

##### Ubuntu 12.04

The following was reported to download and compile the TXS 2.6.6 Version under Ubuntu 12.04
(when newer versions of TXS are released this will probably also work when exchanging the version numbers below with the most recent ones):

```shell
apt-get install build-essential debhelper devscripts qtbase5-dev qt5-default qt5-qmake  libqt5svg5-dev qtscript5-dev qttools5-dev libpoppler-qt5-dev zlib1g-dev pkg-config
wget 'https://github.com/texstudio-org/texstudio/archive/2.12.8.tar.gz' --output-document=texstudio-2.12.8.tar.gz
cp texstudio-2.12.8.tar.gz texstudio_2.12.8.orig.tar.gz
tar -xf texstudio-2.12.8.tar.gz
cd texstudio*
debuild
```
