
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

[bug]: https://tug.org/pipermail/tex-k/2019-May/003014.html


<!--                           < Tip / Trick >                               -->

## Auxiliary Files In Separate Directory

The auxiliary files created by **LaTeX** often clutter the working directory.

Aside from using `Tools › Clean Auxiliary Files` for cleanup,<br>
you may want to have these files in a **separate directory**.

---

### Prepare

You have to *create the directory you want to use*,<br>
as otherwise, **pdflatex** will exit with an error.

###### Multiple Paths

To use multiple paths, ***combine the paths with a separator***.

`<PathA><Separator><PathB>`

|     System    | Separator |
|      ---      |    ---    |
| Linux / MacOS |    `:`    |
|    Windows    |    `;`    |

---

### MiKTeX

1. Enable **Advanced Options**

2. Goto `Options › Configure › Commands`

3. Add `-auxdirectory=` / `-output-directory=` with your location

   `-output-directory` is like `-auxdirectory`<br>
   but also outputs **PDFs** to the specified location.

4. Redirect to `Options › Configure › Build › Build Options`

5. Redirect to `Build Options › Additional Search Paths › Log File`

6. Add your location

7. Only continue if you used `-output-directory=`

8. Redirect to `Build Options › Additional Search Paths › PDF File`

9. Add your location


### TeX Live

1. Enable **Advanced Options**

2. Goto `Options › Configure › Commands`

3. Add `-output-directory=` with your location

4. Redirect to `Options › Configure › Build › Build Options`

5. Redirect to `Build Options › Additional Search Paths › Log File`

6. Add your location

7. Redirect to `Build Options › Additional Search Paths › PDF File`

8. Add your location

---

### BibTeX

For BibTeX you have to modify it's call to<br>
```shell
bibtex.exe -include-directory=your_location
```


### Biber

For Biber you have to modift it's call to<br>
```shell
biber.exe --output_directory=your_location %
```

### PDF Viewer

For the external PDF viewer:

1. Goto `Commands`

2. Set `External PDF Viewer` to (example):

   ```shell
   xdg-open ?p{pdf}:ame > /dev/null
   ```

   *May vary depending on your external PDF viewer*


### Build Scripts

If you use a build script that **generates article images** into your<br>
output directory and those images are **used by your articles**,then <br>
it is adviced to use a **recent version** of **TeXLive** (after `2019/05/07`).

This is because of a [bug] present in earlier versions that prevents<br>
graphics from being located inside the **output directory**.

##### Workaround

If you for some reason cannot update to a more recent<br>
version of **TeXLive**, try the following workaround.

In the **preamble** of your `.tex` & `.cls` files, add:

```tex
%
% Workaround a bug in the \includegraphics macro which
% fails to include images from the output directory.
%
% For more details see https://github.com/latex3/latex2e/issues/145

\def\Gin@getbase#1{%
  \edef\Gin@tempa{%
    \def\noexpand\@tempa####1#1\space{%
      \def\noexpand\Gin@base{####1}}}%
  \@iffileonpath{\filename@area\filename@base#1}%
    {\Gin@tempa
     \expandafter\@tempa\@filef@und
     \edef\Gin@ext{#1}}{}}%
```
