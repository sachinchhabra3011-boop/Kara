# Kara

Kara turns speech into writing, personalised to one speaker, and runs entirely
on the user's own computer.

It exists for people whose speech general dictation software handles badly —
where off-the-shelf recognition is wrong often enough to be unusable, however
clearly the speaker is understood by the people around them. Kara is trained on
recordings of the person who will use it, and that is what makes the difference:
on the voice it was built for, word error rate went from **34.7%** with a general
model to **4.5%**.

## Download

**[Kara-v1.0.zip](Kara-v1.0.zip)** — 403 KB

Unpack it anywhere, then from that folder:

```
powershell -ExecutionPolicy Bypass -File setup.ps1
powershell -ExecutionPolicy Bypass -File install_app.ps1
```

`setup.ps1` installs the Python dependencies and fetches the base speech model on
first use. Windows 10 or 11 and Python 3.12 are required. An NVIDIA GPU is
optional — without one Kara uses a quantised CPU model instead. `install_app.ps1`
adds a Start-menu shortcut, so keep the folder where you put it.

## Teaching it your voice

A fresh install runs the general model and is not personalised yet. Kara offers
to record a short setup on first launch; the recordings stay on your machine, and
training runs there too.

## Moving an existing setup to another computer

On the old machine: **Settings ▸ Backup**, point it at a folder, switch on *Also
copy the trained voice model*, and back up. On the new machine, install as above,
point **Settings ▸ Backup** at the same folder and press **Restore**. The profile
records which trained model belongs to it, so the restored one is found and used.

## Privacy

Everything runs locally. Recordings, documents and the trained voice model stay
on the machine; there is no account and no server. `PRIVACY.md` inside the
download has the detail, including the few optional features that can use the
network and exactly what each of them sends.

Kara is free for personal use.
