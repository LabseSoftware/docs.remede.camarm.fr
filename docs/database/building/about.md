---
layout: default
title: About
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

Le script `scripts/add_word.py` permet d'ajouter un mot rapidement à la base sans la reconstruire...

Il :
- Ajoute votre mot dans `data/mots.txt`
- Ajoute votre mot dans le JSON
- Ajoute votre mot dans `data/remede.db`
- Re-génère l'index de `data/remede.db`

```shell
python3 scripts/add_word.py <word> <phoneme>
```

Pour ajouter plusieurs mots:

`wordlist.txt` (tabulation entre mot et ipa: `mot\t/ipa/`)
```
acupuncture /a.ky.pɔ̃k.tyʁ/
remède  /ʁəmɛd/
```
et exécuter
```shell
python3 scripts/add_word.py -f wordlist.txt
```
