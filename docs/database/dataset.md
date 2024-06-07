---
layout: default
title: Dataset
parent: Database
permalink: /docs/database/dataset
---

# Dataset
The roots of Remède... 
{: .fs-6 .fw-300 }

The `data` folder is destined to the linguistics resources used by Remède.

`data/mots.txt`: List of +245 000 words, comma separated

`data/ipa.json`: For a key 'word', returns his IPA
- Generated from `data/IPA.txt`: a text file of format `[word]\t[ipa]` by `scripts/pre_generate_ressources.py`

`data/REMEDE_a.jon`: The final indexed file ; for a key 'word' returns [his document following the REMEDE schema](https://docs.remede.camarm.fr/docs/database/schema)

`data/remede.db`: A sqlite database ([reference](https://docs.remede.camarm.fr/docs/database/db-schema))

