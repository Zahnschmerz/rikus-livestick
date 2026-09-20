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
| Debian Live | Debian and relatives |
| Arch (archiso) | Arch Linux, EndeavourOS, CachyOS |
| Manjaro (miso) | Manjaro |
| Fedora / dracut | Fedora, **Void Linux**, Solus |
| openSUSE (kiwi) | openSUSE Leap and Tumbleweed |
| Mageia | Mageia |

Two ways of writing, chosen automatically: **file by file** (then a storage area is
possible) or a **1:1 copy** for images that bring their own boot record — FreeBSD, for
example.

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

**1.3 beta** (20 September 2026) — the storage area is fast again, Ubuntu-family sticks
are set up the way those systems expect, and the stick is properly finished and read
back after writing.

⚠️ **Microsoft Surface Go 2:** sticks with Ubuntu, Xubuntu or Linux Mint written by
version 1.3 will not boot on that device. Sticks with Debian, Fedora, Arch, Manjaro,
openSUSE or Mageia are unaffected. If you own a Surface Go 2, please stay on 1.2.

All changes, in German and English: https://livestick.rikus.info/aenderungen

## Where the code lives

This page is the **contact point**, not the source archive. The program is delivered
through the package repository above, not from here.
Use **Issues** for bug reports and questions — that is what this repository is for.

---

© Gilbert Rikus · https://rikus.info
