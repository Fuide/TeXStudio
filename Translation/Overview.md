<!----------------------------[ Navigation Links ]----------------------------->

[‹‹ Overview]: ../README

[Translating]: Translate/Overview
[Grammars]: Grammar/Overview
[Building]: Build/Overview

<!-------------------------------[ Navigation ]-------------------------------->

##### [‹‹ Overview]

##### 『 [Building] 』 「 [Translating] 」 『 [Grammars] 』

---

<!----------------------------[ Translation Links ]---------------------------->

[QT Translation Framework]: http://doc.qt.io/qt-5/qtlinguist-index.html
[Transifex]: https://www.transifex.com/texstudio/texstudio/dashboard/
[Pull Request]: https://github.com/texstudio-org/texstudio/pulls


<!-------------------------------[ Translation ]------------------------------->

# Translation

TexStudio translations are **[Qt Translation Framework]** based.<br>
They can be edited either via **Transifex** or **QtLingust**


### Transifex

In this approach you will have to edit the<br>
**TeXStudio** project **online** via [Transifex].


### QtLingust

<br>

###### Extract Basic

1. Extract translatable strings from source to `.ts` file with
    ```shell
    lupdate
    ```

2. Use **QtLingust** to edit the `.ts` translation files

<br>

###### Extract Additional

1. Extract additional translations for `uiconfig.xml`,<br>
   `color names` and `qnfa format names` with
    ```shell
    texstudio --update-translations
    ```

2. Copy the generated `additionaltranslations.cpp`<br>
   from your build folder to your source folder.

<br>


###### Bundle Edits

1. Compile the `.ts` files to `.qm` files with
    ```shell
    lrelease
    ```

2. Open a **[Pull Request]** or send an **Email** with the `.ts` and `.qm` files


### Notes

Due to how **QtLingust** works, string corrections like spelling<br>
mistakes and capitalization generate new translation strings.

To deal with this, it is adviced to alphabetically sort strings in<br>
**QtLingust** by clicking on the column header to have similar<br>
strings appear next to one another.
