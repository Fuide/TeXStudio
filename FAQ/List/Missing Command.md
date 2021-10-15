
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

[CWL File]: CWL%20File
[Valid Commands]: Valid%20Commands
[Settings Directory]: Settings


<!--                               < FAQ >                                   -->

## Why does a command not auto-complete

First, check if **TeXStudio** know the command.

A command is know, if it is **not** underlined with *red squiggly lines*.

*See [Valid Commands] for more details.*

##### Known

To reduce overcrowding, **TeXStudio** does not<br>
include all commands in the `typical` tab.

More precisely, all commands from auto-generated<br>
`.cwl` files are by default only visible in the `all` tab.

*Check if the command appears in the `all` tab of the completion.*

To change this default behavior of a command,<br>
simply edit the corresponding [CWL File].


##### Unknown

If the command is unknown, the solution is to write a [CWL File]<br>
defining the command and putting it in the [Settings Directory].
