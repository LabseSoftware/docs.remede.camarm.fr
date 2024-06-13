---
layout: default
title: Credits
parent: Database
nav_order: 15
permalink: /docs/database/credits
---

# Credits
Listing of all tools and sources used to create database and serve all app functionalities. 
{: .fs-6 .fw-300 }

Remède creates its own base of french words, synonyms, antonyms with extern services.

- Definitions, examples and etymologies by the [french Wiktionary](https://fr.wiktionary.org/wiki/Wiktionnaire:Page_d%E2%80%99accueil)<sup>[CC BY-SA 3.0 Deed](https://fr.wiktionary.org/wiki/Wiktionnaire:Licence)</sup>, with the API wrapper made by [Frederic Gainza](https://api-definition.fgainza.fr/)<sup>[GPL 3.0](https://github.com/FredGainza/api-definition/blob/main/LICENSE)</sup>, modified by [Labse Software](https://github.com/LabseSoftware/api-definition) for Remède.
- Synonyms from [synonymo.fr](http://www.synonymo.fr)
- Antonyms from [antonyme.org](http://www.antonyme.org)
- Conjugations from [conjuguons.fr](http://www.conjuguons.fr)
- Wordlist and IPA from [Open Dict Data](https://github.com/open-dict-data/ipa-dict)<sup>[MIT](https://github.com/open-dict-data/ipa-dict/blob/master/LICENSE)</sup> ([fr_FR.txt](https://github.com/open-dict-data/ipa-dict/blob/master/data/fr_FR.txt) in their repo)
  - Another IPAs from french Wiktionary (above), words from [Words](https://github.com/lorenbrichter/Words) <sup>[CC0 1.0 Universal](https://github.com/lorenbrichter/Words/blob/master/LICENSE)</sup> by lorenbrichter (see concerned word in [wordlist-Words-CC0-1.0.txt](https://github.com/camarm-dev/remede/tree/main/data/wordlist-Words-CC0-1.0.txt)).
- Rimes are data from [Open Lexicon](http://www.lexique.org/?page_id=91)<sup>[CC BY-SA 4.0 Deed](https://github.com/chrplr/openlexicon/blob/master/LICENSE.txt)</sup>, parsed by the [Drime](https://a3nm.net/git/drime/files.html)<sup>[GPLv3](https://a3nm.net/git/drime/file/COPYING.html)</sup> project to be added to Remède database.
- The TTS service from [nanotts](https://github.com/gmn/nanotts)<sup>[Apache 2.0](https://github.com/gmn/nanotts/blob/master/LICENSE)</sup>, implemented in the API [opentts](https://github.com/synesthesiam/opentts)<sup>[Apache 2.0](https://github.com/gmn/nanotts/blob/master/LICENSE)</sup>, hosted by us
- The corrector service by [languagetool.org](https://languagetool.org)<sup>[LGPL 2.1](https://github.com/languagetool-org/languagetool/blob/master/COPYING.txt)</sup>, hosted by us

<sub>Remède collects these data and merge them to a unique document, served in a database. You can learn more about a specific word credits, in the more menu from the definition page of the application. Transparency about our data provenance is a priority for us at Remède. For more informations, contact us at [software@camarm.dev](mailto:software@camarm.dev).</sub>
