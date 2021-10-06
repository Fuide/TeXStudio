
<!--                            < Static Links >                             -->

[FAQ]: ../../FAQ/Overview
[Tips & Tricks]: ../Overview
[Scripts]: ../../Scripts/Overview
[Build]: ../../Build/Overview
[Contribute]: ../../Contribute/Overview


<!--                             < Navigation >                              -->

##### 『 [FAQ] 』 「 [Tips & Tricks] 」 『 [Scripts] 』 『 [Build] 』『 [Contribute] 』

---


<!--                          < Tip / Trick Links >                          -->

[MikTeX]: http://tex.stackexchange.com/questions/2063/
[TeXLive]: http://tex.stackexchange.com/questions/1137/

[how TXS knows about valid commands]: ../FAQ/List/TXS%20Valid%20Commands
[why TXS marks packages as missing]: ../FAQ/List/TXS%20Missing%20Packages


<!--                           < Tip / Trick >                               -->

## Custom Packages

To have **(pdf) latex** include your `.sty` files when<br>
compiling you will have to let your distribution know.

###### Distribution Specific Instruction:
###### ⟮ [MikTeX] ⟯     ⟮ [TeXLive] ⟯

---

### Package Name

**TXS** obtains information on installed packages from the distribution.


##### TeXLive

Packages will be auto-detected as long as<br>
you make sure to have `texhash` included.

( ***TXS*** *uses the `ls-R` cache* )


##### MikTeX

Currently there is no way to detect packages in a local `texmf` directory.<br>
For details see [why TXS marks packages as missing].

---

### Commands

Please first read [how TXS knows about valid commands] before continuing.

While **TXS** is *technically capable of auto-creating* `cwl` from<br>
`sty` files, it is strongly recommend to explicitly write a `cwl`<br>
file and place it in in the according folder.

For every instance of `\usepackage{<package>}`, **TXS** loads<br>
a `<package>.cwl` and the within contained commands.
