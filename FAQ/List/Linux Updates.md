
<!--                            < Static Links >                             -->

[FAQ]: ../../FAQ/Overview
[Tips & Tricks]: ../Overview
[Scripts]: ../../Scripts/Overview
[Build]: ../../Build/Overview
[Contribute]: ../../Contribute/Overview


<!--                             < Navigation >                              -->

##### 「 [FAQ] 」 『 [Tips & Tricks] 』 『 [Scripts] 』 『 [Build] 』『 [Contribute] 』

---


<!--                             < FAQ Links >                               -->

[OpenSuse]: https://software.opensuse.org/download/package?project=home:jsundermeyer&package=texstudio
[Apt-Pinning]: https://wiki.debian.org/AptPreferences


<!--                               < FAQ >                                   -->

## Keeping TeXStudio up-to-date on Linux

If you want to independently update your **TeXStudio** installation,<br>
head over to [OpenSuse] and select the distribution you are using.

You will be given instructions for manual integration<br>
and in some cases you might have to use [Apt-Pinning].


#### Ubuntu Trusty Tahr (14.04)

```shell
sudo sh -c "echo 'deb http://download.opensuse.org/repositories/home:/jsundermeyer/xUbuntu_14.04/' >> /etc/apt/sources.list.d/owncloud.list"
```

```shell
wget http://download.opensuse.org/repositories/home:/jsundermeyer/xUbuntu_14.04/Release.key
```

```shell
sudo apt key add - < Release.key
sudo apt update
sudo apt install texstudio
```
