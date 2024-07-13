---
layout: default
title: Credits
parent: Database
nav_order: 8
permalink: /docs/database/credits
---

# Credits
Listing of all tools and sources used to create database and serve all app functionalities. 
{: .fs-6 .fw-300 }

Remède creates its own base of french words, synonyms, antonyms with extern services.

## French database credits

- Definitions, examples and etymologies by the [french Wiktionary](https://fr.wiktionary.org/wiki/Wiktionnaire:Page_d%E2%80%99accueil)<sup>[CC BY-SA 3.0 Deed](https://fr.wiktionary.org/wiki/Wiktionnaire:Licence)</sup>, with the API wrapper made by [Frederic Gainza](https://api-definition.fgainza.fr/)<sup>[GPL 3.0](https://github.com/FredGainza/api-definition/blob/main/LICENSE)</sup>, modified by [Labse Software](https://github.com/LabseSoftware/api-definition) for Remède.
- Synonyms from [synonymo.fr](http://www.synonymo.fr)
- Antonyms from [antonyme.org](http://www.antonyme.org)
- Conjugations from [conjuguons.fr](http://www.conjuguons.fr)
- Rhymes dictionary is made with data from [Open Lexicon](http://www.lexique.org/?page_id=91)<sup>[CC BY-SA 4.0 Deed](https://github.com/chrplr/openlexicon/blob/master/LICENSE.txt)</sup>, parsed by the [Drime](https://a3nm.net/git/drime/files.html)<sup>[GPLv3](https://a3nm.net/git/drime/file/COPYING.html)</sup> project to be added to Remède database.
    - Used data: `syllables count`, `elidable` and `femnine`

**Wordlist and IPAs credits**

<sub>Wordlists and IPA are the root of our database: we iterate wordlists and fetch word's informations using the services listed above.</sub>

- Wordlist and IPA from [Open Dict Data](https://github.com/open-dict-data/ipa-dict)<sup>[MIT](https://github.com/open-dict-data/ipa-dict/blob/master/LICENSE)</sup> ([fr_FR.txt](https://github.com/open-dict-data/ipa-dict/blob/master/data/fr_FR.txt) in their repo, [data/fr/IPA.txt](https://github.com/camarm-dev/remede/blob/main/data/fr/IPA.txt) in our repo)
- Another IPAs from french Wiktionary (above), words from [Words](https://github.com/lorenbrichter/Words) <sup>[CC0 1.0 Universal](https://github.com/lorenbrichter/Words/blob/master/LICENSE)</sup> by lorenbrichter (see concerned word in [wordlist-Words-CC0-1.0.txt](https://github.com/camarm-dev/remede/tree/main/data/wordlist-Words-CC0-1.0.txt)).
- Another IPAs from french Wiktionary (above), words from [wiktionaire-fr](https://github.com/drogbadvc/wiktionaire-fr) <sup>[NO LICENCE SPECIFIED](https://github.com/drogbadvc/wiktionaire-fr)</sup> by drogbadvc, data reorganised from [WiktionaryX](http://redac.univ-tlse2.fr/lexiques/wiktionaryx.html) <sup>[CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)</sup> project whose data comes from [Wiktionary Dumps](https://dumps.wikimedia.org/) (see concerned word in [wordlist-wiktionaire-fr.txt](https://github.com/camarm-dev/remede/tree/main/data/wordlist-wiktionaire-fr.txt)).

## English database credits

_English database is not available yet_

- Definitions, examples and etymologies by the [english Wiktionary](https://en.wiktionary.org)<sup>[CC BY-SA 3.0 Deed](https://fr.wiktionary.org/wiki/Wiktionnaire:Licence)</sup>, with the API wrapper made by [Frederic Gainza](https://api-definition.fgainza.fr/)<sup>[GPL 3.0](https://github.com/FredGainza/api-definition/blob/main/LICENSE)</sup>, modified by [Labse Software](https://github.com/LabseSoftware/api-definition) for Remède.
- Synonyms and antonyms from [thesaurus.com](https://www.thesaurus.com)<sup>NO LICENSE SEPCIFIED</sup>
- Conjugations from [???]()

**Wordlist and IPAs credits**

- Wordlist and IPA from [Open Dict Data](https://github.com/open-dict-data/ipa-dict)<sup>[MIT](https://github.com/open-dict-data/ipa-dict/blob/master/LICENSE)</sup> ([en_US.txt](https://github.com/open-dict-data/ipa-dict/blob/master/data/en_US.txt) in their repo, [data/en/IPA.txt](https://github.com/camarm-dev/remede/blob/main/data/en/IPA.txt) in our repo)

## Other services credits

- The TTS service from [nanotts](https://github.com/gmn/nanotts)<sup>[Apache 2.0](https://github.com/gmn/nanotts/blob/master/LICENSE)</sup>, implemented in the API [opentts](https://github.com/synesthesiam/opentts)<sup>[Apache 2.0](https://github.com/gmn/nanotts/blob/master/LICENSE)</sup>, hosted by us
- The corrector service by [languagetool.org](https://languagetool.org)<sup>[LGPL 2.1](https://github.com/languagetool-org/languagetool/blob/master/COPYING.txt)</sup>, hosted by us

<sub>Remède collects these data and merge them to a unique document, served in a database. You can learn more about a specific word credits, in the more menu from the definition page of the application. Transparency about our data provenance is a priority for us at Remède. For more informations, contact us at [software@camarm.dev](mailto:software@camarm.dev).</sub>
