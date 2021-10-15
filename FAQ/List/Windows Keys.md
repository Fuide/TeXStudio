
<!--                            < Static Links >                             -->

[FAQ]: ../../FAQ/
[Tips & Tricks]: ../
[Scripts]: ../../Scripts/
[Build]: ../../Build/
[Contribute]: ../../Contribute/


<!--                             < Navigation >                              -->

##### 「 [FAQ] 」 『 [Tips & Tricks] 』 『 [Scripts] 』 『 [Build] 』『 [Contribute] 』

---


<!--                             < FAQ Links >                               -->

[Windows]: https://en.wikipedia.org/wiki/AltGr_key#Control_.2B_Alt_as_a_substitute


<!--                               < FAQ >                                   -->

## Windows AltGr Problems

Some of **TeXStudios** shortcuts contain <kbd>Ctrl + Alt</kbd><br>
⤷ <kbd>Ctrl + Alt + S</kbd> for `Save As`

##### Problem

[Windows treats <kbd>AltGr</kbd> like <kbd>Ctrl + Alt</kbd>](Windows)

Because of this, you aren't able to type <kbd>AltGr + S</kbd> for example.<br>
*(Corresponds to a certain character on Polish keyboards)*

Instead this would trigger `Save As`.

As there are only a **few such cases** while also being limited to **Windows**,<br>
we do not want to disregard <kbd>Ctrl + Alt</kbd> shortcuts completely.

##### Solution

**TeXStudio** changes / disables known problematic shortcuts<br>
on startup, based on the current keyboard language.

*If you experience problems with certain characters, please*<br>
*report them so they can be added to the exclude list.*

As a workaround you can change the corresponding shortcut in the options.
