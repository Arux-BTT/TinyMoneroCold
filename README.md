# TinyMoneroCold
Easy and secure way to create Monero cold wallet

TinyMoneroCold is a very light Linux distro whose purpose is to facilitate the creation of Monero cold wallets.
The security is crucial. There is no unknown code in TinyMoneroCold. All the content is auditable, see below for further clarification.

## How to use it?

1)Download the iso.

2)Burn it on to a cd or dvd. To use a USB drive, [Rufus](https://rufus.akeo.ie/) is the way to go.

3)Boot the media **on an offline computer**. When the desktop appears, **you can remove the media**. All is running in RAM.


## How secure is it ?

First, all runs in RAM, so if you are offline and if you remove all drives, there's no way to record anything.

Secondly, the tcz extensions comes from http://tinycorelinux.net and are supplied with their md5 checksum. I only added three tcz extensions: gnupgV1symlink.tcz, monero-wallet-generator_c04a4e8.tcz and monero-wallet-cli.x86.v0.10.3.1.tcz.

To audit a tcz extension, use "unsquashfs extension_name.tcz", a directory named "squashfs-root" will be created, containing all the files of the extension.


gnupgV1symlink.tcz is a symlink gpg->gpg2.

monero-wallet-generator_c04a4e8.tcz is the clone of [https://github.com/moneromooo-monero/monero-wallet-generator/](https://github.com/moneromooo-monero/monero-wallet-generator/) and can be checked with GnuPG2.

monero-wallet-cli.x86.v0.10.3.1.tcz is the official 32bits binary from [https://getmonero.org/](https://getmonero.org/downloads/) and can be checked with checksum.

## Stay paranoid !

when you want to store a significant amount of Monero, always use this tool **offline and without any drives**. 
