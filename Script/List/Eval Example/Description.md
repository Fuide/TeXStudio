<!----------------------------[ Navigation Links ]----------------------------->

[‹‹ Overview]: ../../../README

[User Manual]: http://texstudio.sourceforge.net/manual/current/usermanual_en.html
[Dictionaries]: ../../../Dictionary/Overview
[Tips & Tricks]: ../../../Tip/Overview
[Scripts]: ../../Overview
[FAQ]: ../../../FAQ/Overview

<!-------------------------------[ Navigation ]-------------------------------->

##### [‹‹ Overview]

##### 『 [FAQ] 』『 [Tips & Tricks] 』「 [Scripts] 」『 [Dictionaries] 』『 [User Manual] 』  

---

<!-------------------------------[ Script Links ]------------------------------>

[Download]: EvalExample.texsmacro


<!----------------------------------[ Script ]--------------------------------->

# Eval Example

This example executes the current editor text as a script.

*Can be used to write / test new scripts instead*<br>
*of opening the `Edit Macros` dialog every time.*

---

**Eval is dangerous**, can lead to ***Arbitrary Code Execution***<br>
and shouldn't be used in a production setting **!**

---

You can also [Download] this macro.

---

### Code

```js
eval(editor.text());
```

Tested with: `TeXStudio 4.0.0`
