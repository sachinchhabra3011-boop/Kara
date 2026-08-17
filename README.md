# Kara Ã¢â‚¬â€ releases

Built releases of **Kara**, a personalised speech-to-text application for
Windows. This repository holds the download packages and nothing else.

**[Download the latest release Ã¢â€ â€™](../../releases/latest)**

---

## What Kara is

Kara turns speech into writing, personalised to one speaker, and runs entirely
on the user's own computer.

It exists for people whose speech general dictation software handles badly Ã¢â‚¬â€
where off-the-shelf recognition is wrong often enough to be unusable, however
clearly the speaker is understood by the people around them. Kara is trained on
recordings of the person who will use it, which is what makes the difference: on
the voice it was built for, word error rate went from **34.7%** with a general
model to **4.5%**.

Everything runs locally. Recordings, documents and the trained voice model stay
on the machine; there is no account and no server. See `PRIVACY.md` inside the
download for the detail, including the few optional features that can use the
network and what each of them sends.

Kara is provided free of charge for personal use.

## What is in a release

Each release has one `.zip` asset containing the application. Unpack it and run
Kara from the folder Ã¢â‚¬â€ there is no installer step that touches the registry.

Releases are also how existing installations update themselves. Kara can check
this repository on launch and offer the new version; if you have Kara already,
you do not need to download anything by hand.

## Updating an existing installation

In Kara: **Settings Ã¢â€“Â¸ About Ã¢â€“Â¸ Updates**, and set *Where to check* to:

```
https://api.github.com/repos/OWNER/REPO/releases/latest
```

replacing `OWNER/REPO` with this repository's path — copy it from the address
bar above. Kara will then check on launch
and offer any newer version. It sends nothing when it checks Ã¢â‚¬â€ no recordings,
no writing, no identifier.

An update downloads, verifies the payload, keeps the previous version, and
restarts. **If the new version fails to start, the previous one is put back
automatically.** Documents, recordings, the trained model and settings are not
touched by an update.

## Source

**Kara's source code is not in this repository and is not public.** This
repository contains built packages only.

The application bundles open-source components, each under its own licence Ã¢â‚¬â€
these are listed in `THIRD-PARTY-NOTICES.md` inside the download. Notably it
uses Qt (via PySide6) under the LGPL-3.0, and the packages are built as a
folder rather than a single file so those libraries remain replaceable, as that
licence requires.

## Reporting a problem

Open an issue here. Please include the Kara version from the header of the
window, and what you were doing.

Kara can write a diagnostics file for you Ã¢â‚¬â€ **Settings Ã¢â€“Â¸ About Ã¢â€“Â¸ Save
diagnostics**. It contains the technical log and a description of the computer,
and **deliberately excludes** recordings, documents, the sentences the user was
asked to read, and any names taught to the app. Nothing is sent automatically;
you choose whether to attach it, and you can open and read it first.

## Licence and terms

`LICENSE`, `TERMS.md` and `PRIVACY.md` are included in every download.

---

*Kara is not a medical device and is not speech therapy. It should not be
relied on for emergency communication, medical or legal documents, financial
instructions, or anything where a recognition error could cause harm Ã¢â‚¬â€ speech
recognition makes mistakes, including mistakes that change meaning rather than
producing obvious nonsense. Always read what it has written before relying on
it. See `TERMS.md` for the full statement.*
