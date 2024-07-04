---
layout: default
title: Generate my own database
grand_parent: Database
parent: Legacy build
permalink: /docs/database/legacy/build/generate
nav_order: 1
---

# Generate my own database
Learn how to generate your own Remède database ! 
{: .fs-6 .fw-300 }

Please read [Lifecycle](https://docs.remede.camarm.fr/docs/database/build/lifecycle) before.

See also [Quickly add a word](https://docs.remede.camarm.fr/docs/database/build/about).

## 0 - Generate required ressources

```shell
python3 scripts/pre_generate_ressources.py
```

## 1 - Start parsing words

1. Start [api-definition](https://docs.remede.camarm.fr/docs/database/build/about) in local
2. Start `parse.py`
```shell
python3 scripts/parse.py
```
This operation take few days !

> [!NOTE]
> You can select letters to parse using an argument : `python3 scripts/parse.py --letters a,b,c,d,e`
> 
> With this method you can run multiple parse scripts at the same time.

## 2 - Generate the Sqlite database

```shell
python3 generate_sqlite.py
```

## 3 - Generate the search index

```shell
python3 generate_index.py
```

## 4 - Add the rimes dictionary

```shell
python3 build_rimes.py
```

## 5 - Enjoy your own database !

The database situated at `data/remede.db` has been generated successfully, and you can now serve it with the API ! Congratulations !
