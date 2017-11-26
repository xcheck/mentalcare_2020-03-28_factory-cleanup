#### user-login-pic
* /usr/share/pixmaps/faces/ _« Raspbian stretch_
* ~/.face _« Cinnamon_
* ~/.face.icon _« SDDM_


### Debian 9 "Stretch" spin-off Raspbian

```
kde-l10n-de libreoffice-l10n-de libreoffice-help-de (libreoffice-style-galaxy) geany-plugin-spellcheck [firefox-esr-l10n-de]
enchant (aspell-de) hunspell-de-de hyphen-de mythes-de   # /usr/share/myspell/dicts
fonts-crosextra-caladea
fonts-crosextra-carlito
fonts-mathjax
fonts-wqy-microhei
ttf-mscorefonts-installer   # phase shift internal: transition ttf-liberation to fonts-liberation [from extra to optional]
gnome-keyring   # requisite w/ evolution
```

|cmd |conf |rel  
|---|--|--  
| localectl [list-locales¦set-locale] | /etc/locale.conf | Systemd  
| locale | /etc/default/locale |  


#### quote window

>
For an example of well-hinted fonts I personally 
recommend the liberation fonts, but only v1, the 2.0 update broke the world 
class hinting the fonts had, which is why debian has both.
>


```
~$ apt show ttf-liberation 
Package: ttf-liberation
Version: 1:1.07.4-2
Priority: extra
Section: oldlibs
Source: fonts-liberation
Maintainer: Debian Fonts Task Force <pkg-fonts-devel@lists.alioth.debian.org>
Installed-Size: 38,9 kB
Depends: fonts-liberation
Homepage: https://fedorahosted.org/liberation-fonts/
Tag: role::shared-lib
Download-Size: 9.878 B
APT-Sources: http://ftp.de.debian.org/debian stretch/main amd64 Packages
Description: Übergangspaket
 Dieses Übergangspaket kann gefahrlos entfernt werden.
```


```
~$ apt show fonts-liberation
Package: fonts-liberation
Version: 1:1.07.4-2
Priority: optional
Section: fonts
Maintainer: Debian Fonts Task Force <pkg-fonts-devel@lists.alioth.debian.org>
Installed-Size: 2.143 kB
Breaks: ttf-liberation (<< 1.07.0-2)
Replaces: ttf-liberation (<< 1.07.0-2)
Homepage: https://fedorahosted.org/liberation-fonts/
Tag: made-of::font, role::data, x11::font
Download-Size: 827 kB
APT-Manual-Installed: no
APT-Sources: http://ftp.de.debian.org/debian stretch/main amd64 Packages
Description: Schriften mit den gleichen Metriken wie Times, Arial und Courier
 Ein Satz von Schriften mit und ohne Serifen und fester Zeichenbreite von Red
 Hat mit genau den gleichen Metriken wie die (unfreien) Microsoft-Schriften
 Times, Arial und Courier. Durch die identischen Metriken können sie als
 direkter Ersatz der Microsoft-Versionen dienen. Der Name der Schriftfamilie
```


### Windows Fonts

|windows path|linux path  
|---|--  
|%SYTEMROOT%\Fonts|~/.local/share/fonts/  
||/usr/local/share/fonts/  


> sudo fc-cache -f