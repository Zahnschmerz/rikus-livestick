# Rikus LiveStick

**Write a live system to a USB stick — and let it remember your changes.**
Choose an ISO file, plug in the stick, press one button. Free.

➡️ **Website, download and free unlock code: https://livestick.rikus.info**

💡 **Based on an idea by Hans-Josef Rausch** — [sysform.de](https://www.sysform.de) ·
[YouTube: SYSFORM IT LINUXHILFEN](https://www.youtube.com/@sysform-it)

---

## What it does

Rikus LiveStick writes an ISO image to a USB stick and, if you want, adds a **storage
area**. Everything you change inside the live system — settings, files, installed
programs — is still there after switching off.

It recognises which live system the image contains and sets the storage area up the way
**that** system expects it:

| Family | Covers |
|---|---|
| Ubuntu (casper) | Ubuntu, Xubuntu, Kubuntu, Lubuntu, **Linux Mint**, Zorin, elementary |
| Debian Live | Debian, Devuan and relatives |
| Arch (archiso) | Arch Linux, EndeavourOS, CachyOS |
| Manjaro (miso) | Manjaro, BigLinux |
| Fedora / dracut | Fedora, Solus, **Void Linux** |
| openSUSE (kiwi) | openSUSE Tumbleweed and Leap 15.6 |
| Mageia | Mageia |
| PikaOS (booster) | PikaOS |

Two ways of writing, chosen automatically: **file by file** (then a storage area is
possible) or a **1:1 copy** for images that bring their own boot record — FreeBSD, for
example.

⚠️ **Take the live ISO.** Debian, Devuan, Fedora, openSUSE and Mageia also offer installer
images (often named “netinst”, “install” or “DVD”) — with those the stick only becomes an
installer stick and no storage area is possible. The exact files that were tested are
listed on https://livestick.rikus.info under “Tested systems”.

Further settings for those who want them: partition table, target (BIOS/UEFI), file
system (FAT32, NTFS, exFAT, UDF, ext4), cluster size, quick or thorough formatting,
stick health check, help for older computers, and a name with a stick icon.
Light and dark, German and English.

## Install (Debian 13, Linux Mint 22, Ubuntu and relatives)

Add the package repository once:

```sh
sudo install -d /etc/apt/keyrings && sudo curl -fsSL https://apt.rikus.info/rikus-apt.gpg -o /etc/apt/keyrings/rikus.gpg
echo "deb [signed-by=/etc/apt/keyrings/rikus.gpg] https://apt.rikus.info stable main" | sudo tee /etc/apt/sources.list.d/rikus.list
```

Then install:

```sh
sudo apt update && sudo apt install rikus-livestick
```

To remove the repository again:

```sh
sudo rm /etc/apt/sources.list.d/rikus.list /etc/apt/keyrings/rikus.gpg && sudo apt update
```

The program asks once for a personal code. You get it free of charge on
**https://livestick.rikus.info** — enter name and e-mail, the code arrives by mail
straight away and is valid for all free Rikus programs.

## Current version

**1.3** (25 September 2026) — the finished release after the beta. With most systems the
storage area now works through memory: your changes are written to the stick when you shut
down or restart, which makes starting faster and is gentle on the stick — so always shut
down from the menu. The systems keep their own boot menu. Sticks with Linux Mint and
Xubuntu start on the Microsoft Surface Go 2 again; the warning from the beta no longer
applies. “Format only” offers up to eleven file systems.

Tested on real computers with Linux Mint, Xubuntu, Debian, Devuan, Fedora, openSUSE
Tumbleweed and Leap 15.6, Mageia, Void Linux, Solus, Manjaro, EndeavourOS, CachyOS,
BigLinux and PikaOS. Ubuntu itself has not been tested yet.

All changes, in German and English: https://livestick.rikus.info/aenderungen

## Where the code lives

This page is the **contact point**, not the source archive. The program is delivered
through the package repository above, not from here.
Use **Issues** for bug reports and questions — that is what this repository is for.

---

© Gilbert Rikus · https://rikus.info
