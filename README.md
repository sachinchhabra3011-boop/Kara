# Kara

Kara turns speech into writing, personalised to one speaker, and runs entirely
on your own computer.

| | Download |
|---|---|
| Windows 10 or 11 | `Kara-v1.59-windows.zip` |
| macOS 12 or newer | `Kara-v1.57-macos.zip` |

## Installing on Windows

**1. Extract the zip first.** Right-click `Kara-v1.59-windows.zip`, choose
*Extract All…*, then *Extract*. This is not optional — if you open Kara from
inside the zip, Windows unpacks only that one file and nothing else works.
Kara will tell you if this happens.

**2. Open the extracted folder and double-click Kara.** That is the only thing
in the folder you need to touch. The first time it sets Kara up and then starts
it; every time after that it just starts it.

Setting up downloads about **3.3 GB** without an NVIDIA graphics card, or about
**5.9 GB** with one — mostly PyTorch and the speech model. It shows progress
throughout. Python 3.12 is installed for you if it is missing.

The `scripts` folder is for Kara to use, not you. Windows opens `.ps1` files in
Notepad instead of running them.

## Installing on a Mac

**1. Unzip it.** Double-click `Kara-v1.57-macos.zip`.

**2. Move the folder somewhere it can stay** — Applications, or your home
folder. Kara keeps your recordings and trained voice inside it, so it should not
sit in Downloads. Moving it now also avoids a macOS behaviour that runs
downloaded apps from a temporary copy, which stops Kara finding its own files.

**3. Open the folder and double-click `Kara`.** The first time, macOS refuses
it: *"Kara cannot be opened because it is from an unidentified developer."* That
happens to everything downloaded that Apple has not been paid to notarise, and
is not a sign anything is wrong. **Right-click `Kara` and choose Open**, then
click **Open**. You only do this once.

Setup runs in a Terminal window so you can watch it, downloads about **3 GB**,
and opens Kara when it finishes. Python 3.12 is installed into your home folder
and never asks for your password.

Afterwards, press **Cmd+Space** and type `Kara` — it is a real application, so
Spotlight finds it and it keeps its own Dock icon.

macOS asks for two permissions, both naming Kara: the **microphone** the first
time it listens, and **Accessibility** the first time you use *send*, which
types your writing into another program. Kara shows a button that opens the
right settings page. Until you grant it, send copies to the clipboard instead
and you press Cmd+V yourself — nothing is ever lost.

## Speed

With an NVIDIA graphics card, Kara answers in under half a second.

Without one — every Mac, and many PCs — it uses a processor engine instead.
Expect a couple of seconds a sentence on Apple Silicon, around four on a fast
PC, longer on a laptop or an Intel Mac. Settings can drop to a smaller model
that is faster and less accurate.

## Teaching it your voice

A fresh install uses the general speech model and is not personalised yet. Kara
offers to record a short setup on first launch. The recordings stay on your
machine and training runs there too.

On the voice Kara was built for, personalising it cut the word error rate from
about 35% to roughly 4.5% on average. What you get depends on your own voice and
how much you record, and Kara only ever shows you figures measured for you.

## Updating

Kara checks for updates itself and offers them when one is published. You
do not need to download it again — accept the offer and it replaces its own
program files, keeping the previous version so it can go back if anything is
wrong. Your recordings, pages and trained voice model are never touched.

It only ever installs the build for the computer it is running on, and
checks that for itself before changing anything. The check sends nothing
about you and can be switched off in Settings.

## Moving to another computer

Open the profile menu — your initial, top-left. **Export profile…** writes a
single file holding your recordings, trained voice model and pages. On the new
computer, install Kara and use **Import a profile…** in the same menu.

That file is not encrypted and contains your voice recordings. Keep it
somewhere private.

Settings ▸ Backup does the same job on a schedule, into a folder you choose —
point both computers at the same synced folder and press Restore on the new one.

## Removing Kara

On Windows, Kara is listed in **Settings ▸ Apps** — uninstall it from there. It
asks before touching your recordings, pages and trained voice model, and keeps
them unless you confirm, because they cannot be recreated without doing the
setup again.

On a Mac, drag the Kara folder to the Trash. Everything is inside it, so copy
anything you want to keep out first.

## Privacy

Everything runs locally. Recordings, documents and the trained voice model stay
on the machine; there is no account and no server. `PRIVACY.md` has the detail,
including the few optional features that can use the network.

Kara is free for personal use.
