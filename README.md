# Kara

Kara turns speech into writing, personalised to one speaker, and runs entirely
on your own computer. Nothing is uploaded and there is no account.

## Download

| | File | Version |
|---|---|---|
| **Windows 10 or 11** | **[Kara-v1.61-windows.zip](https://github.com/sachinchhabra3011-boop/Kara/releases/download/v1.61/Kara-v1.61-windows.zip)** | 1.61 |
| **macOS 12 or newer** | **[Kara-v1.60-macos.zip](https://github.com/sachinchhabra3011-boop/Kara/releases/download/v1.60/Kara-v1.60-macos.zip)** | 1.60 |

> **Do not download "Source code (zip)".** GitHub adds those two entries to every
> release automatically and they are not Kara — they contain this page and
> nothing else. Use the links above, or the file whose name starts with `Kara-`.

## Installing on Windows

1. Right-click the zip and choose **Extract All**, then **Extract**.
2. Open the folder that appears and double-click **Setup**.
3. Leave it running. It downloads about 3 GB the first time, so it takes a while.
4. Kara opens by itself when it is finished.

Extracting first is not optional. If you open Setup from inside the zip, Windows
unpacks only that one file and nothing else works — Setup notices this and tells
you.

After the first run, press the Windows key and type **Kara** to open it.

Setup installs Python for you if it is missing, and says what to try if anything
stops. The `scripts` folder is for Kara to use, not you.

## Installing on macOS

Extract the zip, then open **Kara** in the folder that appears.

## What it does

Kara learns one person's voice. Out of the box it uses a general speech model;
as you record and train, it adapts to how you actually speak, which matters most
for speech that ordinary dictation software handles badly.

Recordings, the voice model and your writing stay on your machine.
