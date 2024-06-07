---
layout: default
title: Document schema
parent: Database
permalink: /docs/database/schema
---

# The Remède document schema
A Remède word document contains everything about a word stored in Remède's database. 
{: .fs-6 .fw-300 }

JSON schema of an indexed word by Remède looks like:

```json
{
  "synonymes": [
    "acupuncture",
    ...
  ],
  "antonymes": [
    "embrocation",
    ...
  ],
  "etymologies": [
    "Du latin <i>remĕdium</i>."
  ],
  "definitions": [
    {
      "genre": [
        "Nom propre",
        "masculin"
      ],
      "classe": "Nom propre",
      "explications": {
        "1": "(Informatique) Dictionnaire français, open source et gratuit qui a pour objectif de remplacer Antidote."
      },
      "exemples": [
        {
          "contenu": "Tu connais pas <b>Remède</b> ? C'est le meilleur dictionnaire mobile !",
          "sources": "Un utilisateur de Remède, 2024"
        }
      ]
    },
    {
      "genre": [
        "Nom commun",
        "masculin"
      ],
      "classe": "Nom commun",
      "explications": {
        "1": "(Médecine) Substance qui sert à guérir un mal ou une maladie. ",
        "2": "(Sens figuré) Ce qui sert à guérir les maladies de l’âme. ",
        "3": "(Sens figuré) Ce qui sert à prévenir, surmonter ou faire cesser un malheur, un inconvénient ou une disgrâce. ",
        "4": "(En particulier) Lavement. "
      },
      "exemples": [
        {
          "contenu": "<i>Le suc d'une certaine plante appelée par les Caraïbes </i>touloula<i>, et par les Français </i>herbes aux flèches<i>, est, dit-on, le seul <b>remède</b> contre les plaies faites par les flèches empoisonnées avec le suc de mancenilier.</i> ",
          "sources": "(R. P. Jean-Baptiste Labat, <i>Voyages aux iles françaises de l'Amérique</i>, nouvelle édition d'après celle de 1722, Paris&#160;: chez Lefebvre &amp; chez A.-J. Ducollet, 1831, page 75)"
        }
      ]
    }
  ],
  "credits": {
    "name": "page Wiktionnaire",
    "url": "https://fr.wiktionary.org/wiki/rem%C3%A8de"
  },
  "ipa": "/ʁəmɛd/",
  "conjugaisons": {}
}
```

Here are the specifications of each field :

- `synonymes` (`[]string`): List of synonyms
- `antonymes` (`[]string`): List of antonyms
- `etymologies` (`[]string`): List of etymologies
- `exemples` (`[]string`): List of examples
- `definitions` (`[]{}`): List of objects containing a word definition
    - `genre` (`string`): The 'genre' of defined word
    - `classe` (`string`): The grammar class of defined word
    - `explications` (`[]string`): List of possible explanation of defined word
    - `exemples` (`[]string`): List of examples sentences using this word (NOT IMPLEMENTED)
- `credits` (`{}`): Object containing credits of the definitions
    - `name` (`string`): Source name
    - `url` (`string`): Source Url
- `ipa` (`string`): International Phonetic Alphabet pronunciation of the word
- `conjugaisons` (`{}`): Object containing word's conjugations
    - `[nom du mode]` (`{}`): Object containing conjugations' tenses for mode
        - `[nom du temps]` (`{}`): Object containing subjects of tense
            - `[sujet]` (`string`): Verbal form (of `mode, tense, subject`)

