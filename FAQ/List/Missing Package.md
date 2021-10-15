
<!--                            < Static Links >                             -->

[FAQ]: ../
[Tips & Tricks]: ../../Tip/
[Scripts]: ../../Scripts/
[Build]: ../../Build/
[Contribute]: ../../Contribute/



<!--                             < Navigation >                              -->

##### 「 [FAQ] 」 『 [Tips & Tricks] 』 『 [Scripts] 』 『 [Build] 』『 [Contribute] 』

---


<!--                             < FAQ Links >                               -->

[Link]: /


<!--                               < FAQ >                                   -->

## Why is a package marked as missing?

**TeXStudio** tries to determine installed **LaTeX**<br>
packages for package name completion and<br>
missing package import warnings.

#### MikTeX

**TeXStudio** queries **MikTeX** about the<br>
installed packages via `mpm.exe --list`.

###### Note

The list of installed packages is not necessarily the same<br>as
the list of available packages (e.g. you could manually<br>
add packages which are not maintained by **MikTeX**).

It would be more correct to get the information<br>
from the filename database (**FNDB**) in **MikTeX**.

However there doesn't seem to be an API for that<br>
and the **FNDB** itself is a proprietary binary format.

Therefore, `mpm.exe --list` is our best guess for **MikTeX**.
