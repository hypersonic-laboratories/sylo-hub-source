<p align="center"><img src="https://sylo.im/favicon.svg" alt="Sylo" width="72"></p>

# Sylo Hub source

**Your AI, not theirs.**

Sylo is a private personal AI that knows you, works for you and tells no one. Your Sylo keeps what it learns about you sealed on your own devices, and it reads your data only when you say so.

## What the Hub is

The Hub is the catalogue of skills, souls and apps your Sylo can use. A skill teaches your Sylo a job, a soul gives it a way of being with you, and an app is a small tool that lives inside Sylo.

Everything in the Hub is open. Every item is readable by anyone, reviewed by a person at Sylo who has read every line, and signed by Sylo. In the app, the **Audit this** button on any item has your Sylo read the whole thing for you and tell you in plain words what it can reach and whether it does what it says. Apps are personal: you can remix one into your own.

This repository holds the source of every item in the Hub, so you can check any of them before you trust it.

## What is in this repository

Each accepted version of an item has a folder of its own, `<kind>/<id>/v<version>`:

```
skills/<id>/v<version>/    entry.json  body.md  picture.webp  [references/*.md]
souls/<id>/v<version>/     entry.json  body.txt picture.webp
apps/<id>/v<version>/      entry.json  picture.webp  [app.js  manifest.json]
catalogue.json             every published version, and the SHA-256 of each of its files
```

A skill, for example `skills/audit/v1`, is two files you can read in a minute:

```
entry.json   the facts: who it is and what it may touch
  {
    "id": "audit",
    "kind": "skill",
    "version": 1,
    "title": "Audit",
    "subtitle": "Check any skill, soul or app before you trust it",
    "reviewed": "2026-11-03",          the day a person last read every line
    "asks": ["Audit the Remind me skill."],   what you might say to start it
    "uses": ["skill inspect", "chat ask"],    the only commands it may run
    "needs": []                        accounts it needs (mail, calendar, browser...)
  }

body.md      the instructions your Sylo follows, in plain language
  # Audit
  Check one item of the Hub for the person: a skill, a soul or an app. You read it as text and report...
```

Nothing is hidden: if a skill can send mail or open a browser, `uses` and `needs` say so, and the instructions are right there beside them. A version's folder is never changed once it is here. A change to an item is a new version and a new folder.

Apps built into Sylo, such as Remote, run as part of Sylo itself. Their folder holds their Hub page (the words, the pictures and what they reach), and their code is Sylo's own.

## How signing and verification work

Every file an item is made of has a SHA-256 hash, and the hashes are listed in a signed index of the whole Hub. After a person at Sylo has read and accepted the items, the head of that index is signed with a key that is held offline and never sits on a server. Your device already knows the matching public key, so it can check the signature itself and does not have to take anyone's word for it.

When your Sylo opens an item, your device checks that the item's bytes match the hash in the signed index. If one byte differs, or the index was not signed by Sylo's key, the item is refused. The folders here are byte for byte the files that were audited, and `catalogue.json` lists the hash of each one, so you can run the same check yourself:

```
shasum -a 256 skills/audit/v1/body.md
```

and compare it with the entry for that file in `catalogue.json`. "See full source" on an item's page in the app opens the folder of the exact version you have.

## Proposing a skill or an app

Nobody uploads to the Hub. Items are added through a reviewed change in Sylo's own repository, and they reach this one when the catalogue changes. That means a pull request opened here is not taken, but ideas are welcome: open an issue to tell us about a skill or an app you would like to see, or one you have written. A change is accepted only when:

- a person at Sylo has read every line, and sets the `reviewed` date;
- the build's checks pass: the item follows the Hub's format, a skill's `uses` lists exactly the commands its instructions name, its `needs` match those commands, and an app's code passes an audit that refuses hidden network calls, obfuscation and anything that reaches outside what the app declares;
- the pictures fit their size limits, and nothing in the folder goes unused;
- a changed item gets a new `version`, because a published version is never rewritten.

## Get Sylo

- Website: [sylo.im](https://sylo.im)
- Android: [Google Play](https://play.google.com/store/apps/details?id=im.sylo.app)
- Desktop: [sylo.im/download](https://sylo.im/download)

## What is coming

The full source of Sylo, with its apps, its pod and its crypto core, is coming to this GitHub organisation, so the whole of Sylo can be read the way the Hub already can.

## License

Sylo is open source under the GNU Affero General Public License v3.0 (AGPL-3.0).

This repository is a one-way, read-only mirror of the Hub's content.

Source: https://github.com/hypersonic-laboratories/sylo-hub-source
