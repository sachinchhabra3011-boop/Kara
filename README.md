# Kara

Kara turns speech into writing, personalised to one speaker, and runs entirely
on your own computer.

## Installing

**1. Extract the zip first.** Right-click `Kara-v1.1.zip`, choose *Extract
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

Kara runs on the processor if there is no NVIDIA graphics card -- a little over
a second per sentence on a fast machine, slower on a laptop. With a card it is
well under half a second and uses the larger model.

The scripts folder is for Kara to use, not you. Do not double-click the files
in it -- Windows opens .ps1 files in Notepad instead of running them.

## Teaching it your voice

A fresh install uses the general speech model and is not personalised yet. Kara
offers to record a short setup on first launch. The recordings stay on your
machine and training runs there too. On the voice Kara was built for, this took
word error rate from 34.7% to 4.5%.

## Moving an existing setup to another computer

On the old machine: Settings > Backup, point it at a folder, switch on **Also
copy the trained voice model**, and back up. On the new machine, install as
above, point Settings > Backup at the same folder and press Restore. The profile
records which trained model belongs to it, so the restored one is found and used.

## Privacy

Everything runs locally. Recordings, documents and the trained voice model stay
on the machine; there is no account and no server. PRIVACY.md has the detail,
including the few optional features that can use the network.

Kara is free for personal use.
