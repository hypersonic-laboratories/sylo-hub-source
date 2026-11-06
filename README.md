# Sylo Hub source

The public source of every item in the Sylo Hub: its apps, skills and souls.

Each accepted version of an item has a folder of its own, `<kind>/<id>/v<version>`: `skills/audit/v1`, `souls/coach/v2`, `apps/meeting-notes/v1`. The folder
holds every file the Hub's catalogue covers with a hash (the instructions, the code and its manifest, the pictures) and the `entry.json` they were written from.
"See full source" on an item's Hub page opens the folder of the version you have, and the files in it are byte for byte the ones that version was audited as.
A version's folder is never changed once it is here: a change of an item is a new version and a new folder.

`catalogue.json` lists the versions the signed catalogue holds today, and the SHA-256 of each file of each, so a folder can be checked against the catalogue's
own hashes. Apps built into Sylo, such as Remote, run as part of Sylo itself: their folder holds their Hub page (the words, the pictures and what they reach),
and their code is Sylo's own.

This repository is a one-way, read-only mirror of the Hub's content. A pull request here is not taken: changes to an item are made in Sylo and reach this
repository when the Hub's catalogue changes.

Source: https://github.com/hypersonic-laboratories/sylo-hub-source
