
<!--                            < Static Links >                             -->

[FAQ]: ../FAQ/Overview
[Tips & Tricks]: Overview
[Scripts]: ../Scripts/Overview
[Build]: ../Build/Overview
[Contribute]: ../Contribute/Overview


<!--                             < Navigation >                              -->

##### 『 [FAQ] 』 「 [Tips & Tricks] 」 『 [Scripts] 』 『 [Build] 』『 [Contribute] 』

---


<!--                          < Tip / Trick Links >                          -->

[config folder]: ../FAQ/List/Config%20Folder


<!--                           < Tip / Trick >                               -->

## Recognition Of Editor Commands

1. Create a `.cwl` file in the [config folder]

2. For every bibliography created using<br>
   `\newcites{<name>}{Bibliography Title}`,<br>
   add the following lines to the `.cwl` file.

   ```txt
   \citepub{\%<bibid\%>}#c
   \nocitepub{\%<bibid\%>}#c
   \bibliographypub{\%<file\%>}#b
   \bibliographystylepub{\%<style\%>}
   ```
  

3. Goto `config/completion/`

4. Check your generated `.cwl` files.
