<!----------------------------[ Navigation Links ]----------------------------->

[‹‹ Overview]: ../

[Translating]: ../Translation/
[Grammars]: /
[Building]: ../Build/

<!-------------------------------[ Navigation ]-------------------------------->

##### [‹‹ Overview]

##### 『 [Building] 』 『 [Translating] 』 「 [Grammars] 」

---

<!------------------------------[ Grammar Links ]------------------------------>

[Language Specification]: http://texstudio.sourceforge.net/manual/qce/QNFA.html
[Language Definitions]: https://github.com/texstudio-org/texstudio/tree/master/utilities/qxs
[User Manual]: http://texstudio.sourceforge.net/manual/current/usermanual_en.html#LANGUAGEDEF

[ConfigDialog]: https://github.com/texstudio-org/texstudio/blob/master/src/configdialog.cpp

<!---------------------------------[ Grammar ]--------------------------------->

# Writing Grammars

A language is defined as a `.qnfa` file and placed at `utilities/qxs`.


#### Resources
- The [Language Specification]
- Existing [Language Definitions]
- The [User Manual]

#### Highlighting

To bring color to your syntax, you have to add the `format` attribute<br>
and either specify an existing format name or create a new one.

You also have to provide the `id` attribute, which is just an internal<br>
name that you can choose yourself except for certain [Edge Cases][Language Specification].

#### Editable

If a used format should be user-editable, it will have to<br>
be registered in the `ConfigDialog` constructor from<br>
[`configdialog.cpp`][ConfigDialog] with `fmConfig -> addCategory()`.

###### Template

```c++
fmConfig -> addCategory(tr("<Grammar Name>"))
    << "<Format1>"
    << "<Format2>";
```

###### Example

```c++
fmConfig -> addCategory(tr("QtScript"))
    << "qtscript:comment"
    << "qtscript:string"
    << "qtscript:number"
    << "qtscript:keyword"
    << "qtscript:txs-variable"
    << "qtscript:txs-function";
```
