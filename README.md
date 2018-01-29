# Recommended packages for VMs other than Qubes VMs #

A metapackage, which includes recommended packages which are useful within
non-Qubes virtual machines. These are not useful in Qubes, since Qubes already
has native implementations for those.

Safe to remove, if you know what you are doing.

Package: anon-shared-packages-dependencies
Architecture: all
Depends: bzip2, file, lsof, most, pciutils, strace, sysfsutils,
less, haveged, locales, apt-transport-https, apt-transport-tor,
sdwdate, bootclockrandomization, timesanitycheck,
sdwdate-gui, timezone-utc, vbox-disable-timesync, pkg-manager-longer-timeouts,
pkg-manager-no-autoupdate, busybox,
security-misc, ${misc:Depends}
Description: Dependencies for both, Anon-Gateway and Anon-Workstation
# Dependencies for both, Anon-Gateway and Anon-Workstation #

A metapackage, which installs packages which both, Anon-Gateway
and Anon-Workstation, depend on.

Do not remove.

Package: anon-shared-packages-recommended
Architecture: all
Depends: bash-completion, command-not-found, zsh, nano, wget, dnsutils,
iputils-ping, apparmor-utils, gtk2-engines-pixbuf,
apparmor-profile-anondist, udisks2, secure-delete, sudo, net-tools,
anon-icon-pack, gpl-sources-download, anon-iceweasel-warning,
scurl, security-misc, tor-ctrl, uwt, openvpn, ntfs-3g,
usability-misc, menu, man-db, anon-apps-config,
${misc:Depends}
Description: Recommended packages for both, Anon-Gateway and Anon-Workstation
# Recommended packages for both, Anon-Gateway and Anon-Workstation #

A metapackage, which includes recommended packages to ensure, Debian GNU/Linux
standard tools are available and other useful recommended packages.

Safe to remove, if you know what you are doing.

Package: anon-gateway-packages-dependencies
Architecture: all
Pre-Depends: anon-shared-packages-dependencies (= ${source:Version})
Depends: tor, anon-gw-base-files, ipv4-forward-disable,
ipv6-disable, ${misc:Depends}
Conflicts: anon-workstation-packages-dependencies
Description: Dependencies for Anon-Gateway
# Dependencies for Anon-Gateway #

A metapackage, which installs packages which Anon-Gateway
depends on.

Do not remove.

Package: anon-gateway-packages-recommended
Architecture: all
Pre-Depends: anon-shared-packages-dependencies (= ${source:Version})
Depends: tor-geoipdb, tor-arm, obfsproxy, obfs4proxy, flashproxy-client,
fteproxy, onion-grater, open-link-confirmation, onioncircuits,
anon-connection-wizard, ${misc:Depends}
Conflicts: anon-workstation-packages-recommended
Description: Recommended packages for Anon-Gateway
# Recommended packages for Anon-Gateway #

A metapackage, which installs packages, which are recommended for
a Tor Gateway.

Safe to remove, if you know what you are doing.

Package: anon-workstation-packages-dependencies
Architecture: all
Pre-Depends: anon-shared-packages-dependencies (= ${source:Version})
Depends: anon-ws-base-files, ${misc:Depends}
Recommends: anon-workstation-packages-recommended (= ${source:Version})
Suggests: anon-shared-desktop (= ${source:Version}),
anon-workstation-default-applications (= ${source:Version}),
anon-workstation-extra-applications (= ${source:Version})
Conflicts: anon-gateway-packages-dependencies
Description: Dependencies for Anon-Workstation
# Dependencies for Anon-Workstation #

A metapackage, which installs packages which Anon-Workstation
depends on.

Do not remove.

Package: anon-workstation-packages-recommended
Architecture: all
Pre-Depends: anon-shared-packages-dependencies (= ${source:Version})
Depends: xchat-improved-privacy, anon-mixmaster, anon-gpg-tweaks, anon-torchat,
anon-ws-disable-stacked-tor, tb-default-browser,
tb-starter, tb-updater, open-link-confirmation, youtube-dl,
thunderbird, enigmail, xul-ext-torbirdy, pwgen, ricochet-im,
python-msgpack, bindp, codecrypt, gnupg2, gnupg-agent, dirmngr,
${misc:Depends}
Suggests: anon-shared-desktop (= ${source:Version}),
anon-workstation-default-applications (= ${source:Version}),
anon-workstation-extra-applications (= ${source:Version})
Conflicts: anon-gateway-packages-recommended
Description: Recommended packages for Anon-Workstation
# Recommended packages for Anon-Workstation #

A metapackage, which installs packages, which are recommended for
Anon-Workstation, because they are useful for a Tor Workstation.

Feel free to remove if you know what you are doing.

Package: anon-shared-desktop
Architecture: all
Depends: xserver-xorg, xserver-xorg-video-qxl, xserver-xorg-video-fbdev,
xserver-xorg-video-vesa, libgl1-mesa-dri, upower, gtk2-engines-pixbuf,
${misc:Depends}
Suggests: anon-shared-desktop-kde (= ${source:Version})
Description: Desktop Depends
# Desktop Depends #

A metapackage, which installs dependencies for desktop environments,
such as KDE, GNOME, etc.

anon-shared-desktop-kde depends on this package.

Package: anon-shared-desktop-kde
Architecture: all
Depends: anon-shared-desktop (= ${source:Version}), sddm, kde-config-sddm,
plasma-desktop, plasma-desktop-data, kwin-x11, ${misc:Depends}
Suggests: anon-shared-kde-accessibility (= ${source:Version}),
anon-shared-desktop-langpack-kde (= ${source:Version})
Description: Recommended packages for Gateway/Workstation base KDE desktop
# Recommended packages for Gateway/Workstation base KDE desktop #

A metapackage, which installs a minimal, yet complete enough
to contain the very basics, KDE desktop. The Anon-Gateway desktop and the
Anon-Workstation desktop depend on this package.

Safe to remove.

Package: anon-shared-applications-kde
Architecture: all
Depends: kdesudo, kscreen, polkit-kde-agent-1, kdepasswd, kfind,
ksysguard, konsole, kwrite, dolphin, baloo-kf5, ark, systemsettings,
p7zip-full, zip, unzip, khelpcenter, ksystemlog, gtk2-engines-oxygen,
gtk3-engines-breeze, plasma-pa,
kde-config-gtk-style, kde-config-gtk-style-preview,
kde-config-screenlocker, kde-config-sddm, kde-style-oxygen-qt5,
kmenuedit, ${misc:Depends}
Suggests: anon-shared-kde-accessibility (= ${source:Version}),
anon-shared-desktop-langpack-kde (= ${source:Version})
Description: Recommended applications for Gateway/Workstation KDE desktop
# Recommended applications for Gateway/Workstation KDE desktop #

A metapackage, which installs a minimal, yet complete enough
to contain the very basics, KDE applications.

Safe to remove.

Package: anon-shared-kde-accessibility
Architecture: all
Depends: gnome-orca,
console-braille, florence, dasher, kdeaccessibility, kvkbd, kmousetool, kmag,
kmouth, jovie, xbrlapi, festival, qt-at-spi, ${misc:Depends}
Description: KDE accessibility tools
# KDE accessibility tools #

A metapackage, which installs accessibility tools for the KDE desktop.

If not required, can be removed, because they are not crucial for
anonymity, privacy or security.

Package: anon-workstation-default-applications
Architecture: all
Depends: hexchat, vlc, mixmaster, kcalc, okular,
gwenview, libkf5kipi31.0.0, libkf5kipi-data,
kgpg, mat, python-hachoir-core, python-hachoir-parser,
python-pdfrw, python-cairo, python-poppler, python-mutagen, libimage-exiftool-perl, gir1.2-gtk-3.0,
pinentry-qt | pinentry-gtk2 | pinentry-curses | pinentry, ${misc:Depends}
Suggests: anon-shared-desktop (= ${source:Version}),
anon-workstation-extra-applications (= ${source:Version}),
anon-workstation-langpack-common (= ${source:Version})
Description: Recommended default applications for Anon-Workstation
# Recommended default applications for Anon-Workstation #

A metapackage, which installs recommended default applications,
which are useful in a default installation of a Tor Workstation.

Can be removed, if not in use, because they are not crucial for anonymity,
privacy or security.

Package: anon-workstation-extra-applications
Architecture: all
Depends: ${misc:Depends}
Recommends: anon-workstation-packages-recommended (= ${source:Version}),
anon-workstation-default-applications (= ${source:Version}), shutter,
gtk-recordmydesktop, libreoffice, kdenlive, kolourpaint4
Suggests: anon-workstation-langpack-common (= ${source:Version})
Description: Complements anon-workstation-default-applications
# Complements anon-workstation-default-applications #

A metapackage, which installs extra applications, to complement the
default applications.

Does not get installed by default, because extra applications
take too much space and are not required for everyone.

Package: anon-workstation-langpack-common
Architecture: all
Depends: ${misc:Depends}
Recommends: iceweasel-l10n-all | firefox-l10n-all, ttf-dejavu, ttf-liberation, locales-all,
ttf-kacst, ttf-farsiweb, scim-pinyin, scim-tables-zh, scim-uim, ttf-arphic-ukai, ttf-arphic-uming,
culmus, libfribidi0, ttf-indic-fonts, scim-anthy, ttf-khmeros, ttf-unfonts-core, ttf-lao,
ttf-thai-tlwg, xfonts-intl-chinese, xfonts-wqy, xfonts-bolkhov-koi8r-75dpi,
xfonts-bolkhov-koi8r-misc, xfonts-cronyx-koi8r-100dpi
Description: Fonts and language packages for better internationalization support
# Fonts and language packages for better internationalization support #

A metapackage which installs fonts and language packages for better
internationalization support.

Does not get installed by default, because it is largely untested
and needs more work.

Package: anon-shared-desktop-langpack-kde
Architecture: all
Depends: ${misc:Depends}
Recommends: kde-l10n-ar, kde-l10n-bg, kde-l10n-bs,
kde-l10n-ca, kde-l10n-cavalencia, kde-l10n-cs, kde-l10n-da, kde-l10n-de, kde-l10n-el, kde-l10n-engb,
kde-l10n-es, kde-l10n-et, kde-l10n-eu, kde-l10n-fa, kde-l10n-fi, kde-l10n-fr, kde-l10n-ga,
kde-l10n-gl, kde-l10n-he, kde-l10n-hr, kde-l10n-hu, kde-l10n-ia, kde-l10n-id, kde-l10n-is,
kde-l10n-it, kde-l10n-ja, kde-l10n-kk, kde-l10n-km, kde-l10n-ko, kde-l10n-lt, kde-l10n-lv,
kde-l10n-nb, kde-l10n-nds, kde-l10n-nl, kde-l10n-nn, kde-l10n-pa, kde-l10n-pl, kde-l10n-pt,
kde-l10n-ptbr, kde-l10n-ro, kde-l10n-ru, kde-l10n-si, kde-l10n-sk, kde-l10n-sl, kde-l10n-sr,
kde-l10n-sv, kde-l10n-tg, kde-l10n-th, kde-l10n-tr, kde-l10n-ug, kde-l10n-uk, kde-l10n-vi,
kde-l10n-wa, kde-l10n-zhcn, kde-l10n-zhtw, anon-workstation-langpack-common (= ${source:Version})
Description: Extra language support for the KDE desktop
# Extra language support for the KDE desktop #

A metapackage, which includes extra language support for the
KDE desktop.

Does not get installed by default, because it takes a lot of
space and requires a better solution.

Package: apparmor-profiles-whonix
Architecture: all
Depends: apparmor-profile-icedove,
apparmor-profile-torbrowser, apparmor-profile-virtualbox,
apparmor-profile-xchat,
apparmor-profile-gwenview, apparmor-profile-okular, ${misc:Depends}
Description: Extra AppArmor profiles developed by the Whonix team
# Extra AppArmor profiles developed by the Whonix team #

A metapackage, which installs apparmor profiles developed by the Whonix team.

Increases security.

Safe to remove, if you know what you are doing.

Package: whonix-gateway-packages-dependencies-pre
Architecture: all
Depends: whonix-gw-network-conf, anon-base-files,
${misc:Depends}
Description: Dependencies for Whonix-Gateway that changes network related files
# Dependencies for Whonix-Gateway that changes network related files #

A metapackage, which installs packages which Whonix-Gateway
depends on. Can not be merged into whonix-gateway-packages-dependencies due to
conflicts with chroot build process.

Do not remove.

Package: whonix-gateway-packages-dependencies
Architecture: all
Pre-Depends: whonix-shared-packages-dependencies (= ${source:Version})
Depends: anon-gateway-packages-dependencies, anon-gw-anonymizer-config,
whonix-gateway-packages-dependencies-pre, ${misc:Depends}
Conflicts: whonix-workstation-packages-dependencies
Description: Dependencies for Whonix-Gateway
# Dependencies for Whonix-Gateway #

A metapackage, which installs packages which Whonix-Gateway
depends on.

Do not remove.

Package: whonix-gateway-packages-recommended
Architecture: all
Pre-Depends: whonix-shared-packages-dependencies (= ${source:Version})
Depends: whonix-gw-desktop-shortcuts, whonix-setup-wizard, ${misc:Depends}
Recommends: anon-gateway-packages-recommended
Conflicts: whonix-workstation-packages-recommended
Description: Recommended packages for Whonix-Gateway
# Recommended packages for Whonix-Gateway #

A metapackage, which installs packages, which are recommended for
Whonix-Gateway.

Safe to remove, if you know what you are doing.

Package: whonix-shared-packages-dependencies
Architecture: all
Pre-Depends: whonix-legacy
Depends: whonix-base-files, anon-apt-sources-list, whonix-firewall,
whonix-initializer, whonixsetup, whonix-repository, grub-enable-apparmor,
${misc:Depends}
Description: Dependencies for Whonix-Gateway and Whonix-Workstation
# Dependencies for Whonix-Gateway and Whonix-Workstation #

A metapackage, which installs packages which both, Whonix-Gateway
and Whonix-Workstation, depend on.

Do not remove.

Package: whonix-shared-packages-recommended
Architecture: all
Depends: anon-shared-packages-recommended, whonixcheck,
${misc:Depends}
Description: Recommended packages for Whonix-Gateway and Whonix-Workstation
# Recommended packages for Whonix-Gateway and Whonix-Workstation #

A metapackage, which includes recommended packages to ensure, Whonix
standard tools are available and other useful recommended packages.

Safe to remove, if you know what you are doing.

Package: whonix-workstation-packages-dependencies-pre
Architecture: all
Depends: whonix-ws-network-conf, anon-ws-dns-conf, anon-base-files,
${misc:Depends}
Description: Dependencies for Whonix-Workstation that changes network related files
# Dependencies for Whonix-Workstation that changes network related files #

A metapackage, which installs packages which Whonix-Workstation
depends on. Can not be merged into whonix-workstation-packages-dependencies
due to conflicts with chroot build process.

Do not remove.

Package: whonix-workstation-packages-dependencies
Architecture: all
Pre-Depends: whonix-shared-packages-dependencies (= ${source:Version})
Depends: whonix-workstation-packages-dependencies-pre,
${misc:Depends}
Recommends: whonix-workstation-packages-recommended (= ${source:Version})
Conflicts: whonix-gateway-packages-dependencies
Description: Dependencies for Whonix-Workstation
# Dependencies for Whonix-Workstation #

A metapackage, which installs packages which Whonix-Workstation
depends on.

Do not remove.

Package: whonix-workstation-packages-recommended
Architecture: all
Depends: whonix-ws-desktop-shortcuts, whonix-ws-irc-chat-support,
whonix-welcome-page, whonix-ws-start-menu-additions,
${misc:Depends}
Recommends: anon-workstation-packages-recommended
Description: Recommended packages for Whonix-Workstation
# Recommended packages for Whonix-Workstation #

A metapackage, which installs packages, which are recommended for
Whonix-Workstation, because they are useful for a Tor Workstation.

Feel free to remove if you know what you are doing.

Package: whonix-gateway-shared-packages-shared-meta
Architecture: all
Pre-Depends: whonix-legacy
Depends: whonix-gateway-packages-dependencies-pre,
anon-shared-packages-dependencies,
anon-shared-packages-recommended,
anon-shared-applications-kde,
whonix-shared-packages-dependencies,
whonix-shared-packages-recommended,
anon-gateway-packages-dependencies,
anon-gateway-packages-recommended,
whonix-gateway-packages-dependencies,
whonix-gateway-packages-recommended,
${misc:Depends}
Description: Whonix-Gateway Shared Packages
# Whonix-Gateway Shared Packages #

A metapackage, which installs packages, for a Whonix-Default-Gateway.

It is shared between Qubes-Whonix and Non-Qubes-Whonix.

It will install build chroot scripts, but not run them.

Feel free to remove if you know what you are doing.

Package: whonix-workstation-shared-packages-shared-meta
Architecture: all
Pre-Depends: whonix-legacy
Depends: whonix-workstation-packages-dependencies-pre,
anon-shared-packages-dependencies,
anon-shared-packages-recommended,
anon-shared-applications-kde,
whonix-shared-packages-dependencies,
whonix-shared-packages-recommended,
anon-workstation-packages-dependencies,
anon-workstation-packages-recommended,
anon-workstation-default-applications,
whonix-workstation-packages-dependencies,
whonix-workstation-packages-recommended,
${misc:Depends}
Description: Whonix-Workstation Shared Packages
# Whonix-Workstation Shared Packages #

A metapackage, which installs packages, for a Whonix-Default-Workstation.

It is shared between Qubes-Whonix and Non-Qubes-Whonix.

It will install build chroot scripts, but not run them.

Feel free to remove if you know what you are doing.

Package: qubes-whonix-gateway
Architecture: all
Depends: whonix-gateway-shared-packages-shared-meta, qubes-whonix,
qubes-whonix-shared-packages-recommended,
qubes-whonix-gateway-packages-recommended, ${misc:Depends}
Replaces: whonix-gateway
Description: Default packages for Qubes-Whonix-Gateway
# Default packages for Qubes-Whonix-Gateway #

A metapackage, which installs packages, for a
Qubes-Whonix-Default-Gateway.

Only depends on whonix-gateway-shared-packages-shared-meta,
because installing anon-shared-desktop is not required in
Qubes-Whonix.

Feel free to remove if you know what you are doing.

Package: qubes-whonix-workstation
Architecture: all
Depends: whonix-workstation-shared-packages-shared-meta, qubes-whonix,
qubes-whonix-shared-packages-recommended,
qubes-whonix-workstation-packages-recommended, ${misc:Depends}
Replaces: whonix-workstation
Description: Default Packages for Qubes-Whonix-Workstation
# Default Packages for Qubes-Whonix-Workstation #

A metapackage, which installs packages, for a
Qubes-Whonix-Default-Workstation.

Only depends on whonix-workstation-shared-packages-shared-meta,
because installing anon-shared-desktop is not required in
Qubes-Whonix.

Feel free to remove if you know what you are doing.

Package: non-qubes-whonix-gateway
Architecture: all
Depends: whonix-gateway-shared-packages-shared-meta, non-qubes-vm-enhancements,
anon-shared-desktop, anon-shared-desktop-kde,
${misc:Depends}
Replaces: whonix-gateway
Description: Default Packages for Non-Qubes-Whonix-Gateway
# Default Packages for Non-Qubes-Whonix-Gateway #

A metapackage, which installs packages, for a
Non-Qubes-Whonix-Default-Gateway.

Depends on whonix-gateway-shared-packages-shared-meta,
and anon-shared-desktop because that is required in
Non-Qubes-Whonix in order to get graphical desktop environment.

Feel free to remove if you know what you are doing.

Package: non-qubes-whonix-workstation
Architecture: all
Depends: whonix-workstation-shared-packages-shared-meta, non-qubes-vm-enhancements,
anon-shared-desktop, anon-shared-desktop-kde,
${misc:Depends}
Replaces: whonix-workstation
Description: Default Packages for Non-Qubes-Whonix-Workstation
# Default Packages for Non-Qubes-Whonix-Workstation #

A metapackage, which installs packages, for a
Non-Qubes-Whonix-Default-Workstation.

Depends on whonix-workstation-shared-packages-shared-meta,
and anon-shared-desktop because that is required in
Non-Qubes-Whonix in order to get graphical desktop environment.

Feel free to remove if you know what you are doing.

(This package description has been [automatically](https://github.com/Whonix/whonix-developer-meta-files/blob/master/debug-steps/packaging-helper-script) extracted and mirrored from `debian/control`.)

# Generic Readme #
## Readme Version ##

[Generic Readme](https://github.com/Whonix/whonix-developer-meta-files/blob/master/README_generic.md) Version 0.3

## Cooperating Anonymity Distributions ##

[Generic Readme](https://github.com/Whonix/whonix-developer-meta-files/blob/master/README_generic.md) beings here. Have a look into the `man` sub folder (if available).

The functionality of this package was once exclusively available in the [Whonix](https://www.whonix.org) ([github](https://github.com/Whonix/Whonix)) anonymity distribution.

Because multiple projects and individuals stated interest in various of Whonix's functionality (examples: [Qubes OS](http://qubes-os.org/trac) ([discussion](https://groups.google.com/forum/#!topic/qubes-devel/jxr89--oGs0)); [piratelinux](https://github.com/piratelinux) ([discussion](https://github.com/adrelanos/VPN-Firewall/commit/6147f0e606377f5a801e98daf22e24ba2c750a21#commitcomment-6360713))), it's best to share as much source code as possible, it's best to share certain characteristics [(such as /etc/hostname etc.) among all anonymity distributions](https://mailman.boum.org/pipermail/tails-dev/2013-January/002457.html)) Whonix has been split into [multiple separate packages](https://github.com/Whonix).

## Generic Packaging ##

Files in `etc/...` in root source folder will be installed to `/etc/...`, files in `usr/...` will be installed to `/usr/...` and so forth. This should make renaming, moving files around, packaging, etc. very simple. Packaging of most packages looks very similar.

## How to use outside of Debian or derivatives ##

Although probably due to generic packaging not very hard. Still, this requires developer skills. [Ports](https://en.wikipedia.org/wiki/Porting) welcome!

## How to Build deb Package ##

See comments below and [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/apparmor-profile-torbrowser).

* Replace `apparmor-profile-torbrowser` with the actual name of this package (equals the root source folder name of this package after you git cloned it).
* You only need [config-package-dev](https://packages.debian.org/wheezy/config-package-dev), when it is listed in the `Build-Depends:` field in `debian/control`.
* Many packages do not have signed git tags yet. You may request them if desired.
* We might later use a [documentation template](https://www.whonix.org/wiki/Template:Build_Documentation_Build_Package).

## How to install in Debian using apt-get ##

Binary packages are available in Whonix's APT repository. By no means you are required to use the binary version of this package. This might be interesting for users of Debian and derivatives. **Note, that usage of this package outside of Whonix is untested and there is no maintainer that supports this use case.**

1\. Get [Whonix's Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key).

2\. Add Whonix's Signing Key to apt-key.

```
gpg --export 916B8D99C38EAF5E8ADC7A2A8D66066A2EEACCDA | sudo apt-key add -
```

3\. Add Whonix's APT repository.

```
echo "deb http://deb.whonix.org jessie main" > /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install this package. Replace `package-name` with the actual name of this package.

```
sudo apt-get install package-name
```

## Cooperation ##

Most welcome. [Ports](https://en.wikipedia.org/wiki/Porting), distribution maintainers, developers, patches, forks, testers, comments, etc. all welcome.

## Contact ##

* Professional Support: https://www.whonix.org/wiki/Support#Professional_Support
* Free Forum Support: https://www.whonix.org/forum
* Github Issues
* twitter: https://twitter.com/Whonix

## Donate ##

* [Donate](https://www.whonix.org/wiki/Donate)
