# Kara for Mac

Kara turns speech into writing, personalised to one speaker, and runs entirely
on your own computer.

## Installing

**1. Unzip it.** Double-click `Kara-v1.54-macos.zip`. macOS unpacks the whole
folder for you.

**2. Move the folder somewhere it can stay** — your Applications folder, or
your home folder. Kara keeps your recordings and trained voice inside it, so it
should not live in Downloads where it might be cleared out. Moving it now also
avoids a macOS security behaviour that runs downloaded apps from a temporary
copy, which stops Kara finding its own files.

**3. Open the folder and double-click `Kara`** — the one with the orange
Kara icon. That is a real Mac application.

The first time, macOS will refuse it: *"Kara cannot be opened because it is
from an unidentified developer."* This is Gatekeeper, and it happens to
everything downloaded from the internet that Apple has not been paid to
notarise. It is not a sign that anything is wrong.

To get past it, **right-click `Kara` and choose Open**, then click **Open** in
the dialog. You only do this once.

Setup then runs in a Terminal window so you can watch it — it downloads about
**3 GB**, mostly PyTorch and the speech model, and takes a while on a slow
connection. When it finishes, Kara opens on its own.

You need macOS 12 or newer. Python 3.12 is installed for you if it is missing,
into your home folder — it does **not** ask for your password and does not
touch the system Python.

### Finding Kara afterwards

Once setup has run, **press Cmd+Space and type `Kara`**. It is a registered
application, so Spotlight finds it, it keeps its own Dock icon, and you never
need to go back to the folder.

If Spotlight does not find it, open the folder and double-click `Kara` once
more — setup registers it with macOS on every run. There is also a plain
`Kara.command` in the folder that starts it from Terminal, as a fallback.

## The two permissions macOS will ask for

Kara needs two things that macOS guards, and it will not work properly without
them. Both prompts name **Kara**, because Kara is a real application.

**Microphone** — asked for the first time Kara listens. Say yes. If you say no,
Kara records silence and does not report an error.

**Accessibility** — needed only for *send*, which puts your writing straight
into Word, Mail or a browser. macOS never asks for this on its own. Kara shows
you a button that opens the right page when you first use send:

> System Settings ▸ Privacy & Security ▸ Accessibility

Switch Kara on there, then quit and reopen Kara. Until you do, send still
copies your writing to the clipboard and you press **Cmd+V** in the document
yourself — nothing is ever lost.

Because Kara is not signed by Apple, macOS ties these permissions to where the
folder is. If you move the Kara folder later, you may have to grant them again.

## Speed

There is no CUDA on any Mac — Apple has not shipped an NVIDIA graphics card
since 2013 — so Kara uses the same processor engine the Windows version uses on
machines without an NVIDIA card. On Apple Silicon this is quick: expect a
couple of seconds per sentence on the medium model, less on small. Settings can
drop to a smaller, faster, less accurate model.

Intel Macs work but are noticeably slower; the small model is the usable one
there.

## Teaching it your voice

A fresh install uses the general speech model and is not personalised yet. Kara
offers to record a short setup on first launch. The recordings stay on your
machine and training runs there too.

Training on a Mac runs in full precision on the processor. It is slower than a
Windows machine with a good NVIDIA card, and Kara measures your own machine and
tells you the real figure before you commit to it.

## Reading aloud

Kara uses the voices already on your Mac — Samantha, Daniel, Karen and the
rest — and can also download higher-quality Piper voices from Settings.

Apple ships a number of novelty voices (Bahh, Boing, Jester and so on) in the
same list as the real ones. Kara hides those rather than risk reading your
writing back in one of them.

## Removing Kara

Drag the Kara folder to the Trash. That is all of it — Kara does not install
anything outside its own folder except a small lock file in
`~/Library/Application Support/Kara`, which you can delete too.

macOS may keep showing Kara in Spotlight for a short while after the folder is
gone; it clears on its own once the index catches up.

Your recordings, pages and trained voice model are inside the folder, so make a
copy first if you want to keep them.

## Everything else

The rest of Kara works the same as it does on Windows — profiles, backup,
export, updates and the privacy guarantees. See `README.md` and `PRIVACY.md`.

Kara is free for personal use.
