---
layout: default
title: Dataset
parent: Database
permalink: /docs/database/dataset
nav_order: 2
---

# Dataset
The roots of Remède... 
{: .fs-6 .fw-300 }

The `data` folder is destined to the linguistics resources used by Remède.

`data/mots.txt`: List of ~1 000 000 words, comma separated

`data/ipa.json`: For a key 'word', returns his IPA
- Generated from `data/IPA.txt`: a text file of format `[word]\t[ipa]` by `scripts/pre_generate_ressources.py`

{: .note }
> The `data/remede.db` file is not included in git files, see [Setup](/docs/develop/setup#fetch-database) to download it.

- `data/remede.schema.json`: JSON schema of [Remède document](/docs/database/schema)
- `data/custom_words.json`:  File to add custom words... The words documents must follow the [Remède Document Schema](/docs/database/schema)
  - `data/custom_words.schema.json`:  its JSON schema

`data/remede.db`: A sqlite database ([reference](https://docs.remede.camarm.fr/docs/database/db-schema))
`data/drime.db`: The [Open Lexicon](http://lexique.org/shiny/openlexicon/) french database rewrote by the project [drime](https://a3nm.net/git/drime/files.html). Useful to get precise word metadata like syllables.

