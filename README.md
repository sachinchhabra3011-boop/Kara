# Kara

Kara turns speech into writing, personalised to one speaker, and runs entirely
on your own computer.

## Installing

Kara runs on Windows and on macOS. Pick the download for your computer.

| | Download | Version |
|---|---|---|
| Windows 10 or 11 | `Kara-v1.53.zip` | 1.53 |
| macOS 12 or newer | `Kara-v1.55-macos.zip` | 1.55 |

The two version numbers differ only because the Mac build came later. They are
the same Kara.

### On Windows

**1. Extract the zip first.** Right-click `Kara-v1.53.zip`, choose *Extract
All...*, then *Extract*. This step is not optional -- if you open Kara from
inside the zip, Windows unpacks only that one file and nothing else works. Kara
will tell you if this happens.

**2. Open the extracted folder and double-click Kara.**

That is the only thing in this folder you need to touch. The first time, it sets
Kara up and then starts it. Every time after that it just starts it.

Setting up downloads about **3.3 GB** on a computer without an NVIDIA graphics
card, or about **5.9 GB** with one -- most of it PyTorch and the speech model.
Expect it to take a while on a slow connection. It shows progress throughout.

You need Windows 10 or 11. Python 3.12 is installed for you if it is missing.

Kara runs on the processor if there is no NVIDIA graphics card. Expect around
four seconds per sentence on a fast machine and longer on a laptop; Settings
can drop to a smaller, faster, less accurate model. With an NVIDIA card the
same model answers in under half a second.

The scripts folder is for Kara to use, not you. Do not double-click the files
in it -- Windows opens .ps1 files in Notepad instead of running them.

### On a Mac

**1. Unzip it.** Double-click `Kara-v1.55-macos.zip`. macOS unpacks the whole
folder for you.

**2. Move the folder somewhere it can stay** -- your Applications folder, or
your home folder. Kara keeps your recordings and trained voice inside it, so it
should not sit in Downloads. Moving it now also avoids a macOS security
behaviour that runs downloaded apps from a temporary copy, which stops Kara
finding its own files.

**3. Open the folder and double-click `Kara`.**

The first time, macOS refuses it: *"Kara cannot be opened because it is from an
unidentified developer."* That happens to everything downloaded from the
internet that Apple has not been paid to notarise, and is not a sign anything is
wrong. **Right-click `Kara` and choose Open**, then click **Open**. You only do
this once.

Setup runs in a Terminal window so you can watch it. It downloads about **3 GB**
and opens Kara when it finishes. Python 3.12 is installed for you if it is
missing, into your home folder -- it never asks for your password.

Afterwards, press **Cmd+Space and type `Kara`**. It is a real application, so
Spotlight finds it and it keeps its own Dock icon.

macOS will ask for two permissions, both naming Kara: the **microphone** the
first time it listens, and **Accessibility** the first time you use *send*,
which types your writing into another program. Kara shows a button that opens
the right settings page. Until you grant it, send still copies to the clipboard
and you press Cmd+V.

There is no CUDA on any Mac, so Kara uses the processor engine -- on Apple
Silicon expect a couple of seconds a sentence. `README-macOS.md` has the detail.

## Teaching it your voice

A fresh install uses the general speech model and is not personalised yet. Kara
offers to record a short setup on first launch. The recordings stay on your
machine and training runs there too. On the voice Kara was built for, personalising it cut the word error rate
from about 35% to roughly 4.5% on average. What you get depends on your own
voice and how much you record, and Kara only ever shows you figures measured
for you.

## Moving an existing setup to another computer

On the old machine: Settings > Backup, point it at a folder, switch on **Also
copy the trained voice model**, and back up. On the new machine, install as
above, point Settings > Backup at the same folder and press Restore. The profile
records which trained model belongs to it, so the restored one is found and used.

## Updating

Kara checks for updates itself and offers them when one is published. You
do not need to download it again -- accept the offer and it replaces its own
program files, keeping the previous version so it can go back if anything is
wrong. Your recordings, pages and trained voice model are never touched.

The check asks one public file which version is current. It sends nothing
about you, and it can be switched off in Settings.

## Moving to a new computer

Open the profile menu (your initial, top-left). **Export profile…** writes a
single file with your recordings, trained voice model and pages in it. On the
new computer, install Kara and use **Import a profile…** in the same menu.

That file is not encrypted and contains your voice recordings -- keep it
somewhere private.

## Removing Kara

On Windows, Kara is listed in **Settings > Apps** -- uninstall it from there.
That removes the shortcuts and the entry. It asks before touching your
recordings, your pages and your trained voice model, and keeps them unless
you confirm, because they cannot be recreated without doing the setup again.

On a Mac, drag the Kara folder to the Trash. Everything is inside it, so copy
your recordings and trained voice model out first if you want to keep them.

## Privacy

Everything runs locally. Recordings, documents and the trained voice model stay
on the machine; there is no account and no server. PRIVACY.md has the detail,
including the few optional features that can use the network.

Kara is free for personal use.
