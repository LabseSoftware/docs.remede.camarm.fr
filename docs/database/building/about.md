---
layout: default
title: About
grand_parent: Database
parent: Building database
permalink: /docs/database/build/about
nav_order: 2
---

# About
This section contains documentation for related resources to Remède generation. 
{: .fs-6 .fw-300 }

## Api Définition

This API, written by [Frederic Gainza](https://api-definition.fgainza.fr/), scrap the [French Wictionary](https://fr.wiktionary.org/wiki/Wiktionnaire:Page_d%E2%80%99accueil).

For Remède, **it has been readapted** by [Labse Software](https://github.com/LabseSoftware/api-definition)

### Start with docker

This API's code is contained under the `api-definition` folder which is a **git submodule**.

In `api-definition` folder:
```shell
docker build -t remede-definition-api . && docker run -p 8089:80 remede-definition-api
```

## Quickly add a word

The script `scripts/add_word.py` let you add a word to the Remède database without rebuilding it totally.

It :
- Add your word in `data/mots.txt`
- Add your word's generate Remède document in JSON files
- Add your word's document in `data/remede.db`
- Re-generated the search index of `data/remede.db`

```shell
python3 scripts/add_word.py <word> <phoneme>
```

To add multiple words:

`wordlist.txt` (tabulation between word and IPA: `mot\t/ipa/`)
```
acupuncture /a.ky.pɔ̃k.tyʁ/
remède  /ʁəmɛd/
```
and execute
```shell
python3 scripts/add_word.py -f wordlist.txt
```
