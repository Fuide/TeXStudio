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

<!---------------------------------[ Mac Links ]------------------------------->



<!-----------------------------------[ Mac ]----------------------------------->

# Mac Build

On Mac you will need to install **Homebrew**.


```shell
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

---

### Dependencies

The dependencies can be installed with:

```shell
brew install qt
brew install poppler
brew install pkg-config
```

---

### Building

Please navigate to the **TeXStudio** source folder.

###### Method 1

Build with **QMake**.

```shell
qmake texstudio.pro
make -j 4
```

###### Method 2

Use the `./BUILD.sh` script.

*This only works if `$PATH` is set correctly,*<br>
*which by default, it is not.*

###### Afterwards

You should now find the `texstudio.app` file in your source folder.


---

### Debug Version

When building the debug version, **Qt5UiTools**<br>
seems to have `libQt5Uitools_debug.a` missing.

###### Workaround

Copy `libQt5Uitools.a` to `libQt5Uitools_debug.a`.

*Probably won't work for* ***QT6***

---

### DMG For OSX 10.8

```shell
macdeployqt texstudio.app -dmg
```
