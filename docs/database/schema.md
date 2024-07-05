---
layout: default
title: Document schema
parent: Database
permalink: /docs/database/schema
nav_order: 4
---

# The Remède document schema
A Remède word document contains everything about a word stored in Remède's database. 
{: .fs-6 .fw-300 }

[Download Remède Document JSON Schema](https://github.com/camarm-dev/remede/tree/main/data/remede.schema.json){: .btn .btn-outline .fs-5 .mb-4 .mb-md-0 }

Or use it into your JSON files:
```JSON
{
  "$schema": "https://remede.camarm.fr/schema.json"
}
```

JSON schema of an indexed word by Remède looks like:

```json
{
  "synonyms": [
    "acupuncture",
    ...
  ],
  "antonyms": [
    "embrocation",
    ...
  ],
  "etymologies": [
    "Du latin <i>remĕdium</i>."
  ],
  "definitions": [
    {
      "gender": "masculin",
      "nature": "Nom propre",
      "explanations": [
        "(Informatique) Dictionnaire français, open source et gratuit qui a pour objectif de remplacer Antidote."
      ],
      "examples": [
        {
          "content": "Tu connais pas <b>Remède</b> ? C'est le meilleur dictionnaire mobile !",
          "sources": "Un utilisateur de Remède, 2024"
        }
      ],
      "plurals": []
    },
    {
      "gender": "masculin",
      "nature": "Nom commun",
      "explanations": [
        "(Médecine) Substance qui sert à guérir un mal ou une maladie. ",
        "(Sens figuré) Ce qui sert à guérir les maladies de l’âme. ",
        "(Sens figuré) Ce qui sert à prévenir, surmonter ou faire cesser un malheur, un inconvénient ou une disgrâce. ",
        "(En particulier) Lavement. "
      ],
      "examples": [
        {
          "content": "<i>Le suc d'une certaine plante appelée par les Caraïbes </i>touloula<i>, et par les Français </i>herbes aux flèches<i>, est, dit-on, le seul <b>remède</b> contre les plaies faites par les flèches empoisonnées avec le suc de mancenilier.</i> ",
          "sources": "(R. P. Jean-Baptiste Labat, <i>Voyages aux iles françaises de l'Amérique</i>, nouvelle édition d'après celle de 1722, Paris&#160;: chez Lefebvre &amp; chez A.-J. Ducollet, 1831, page 75)"
        }
      ],
      "plurals": [
        {
          "label": "Masculin",
          "singular": "remède",
          "plural": "remèdes"
        }
      ]
    }
  ],
  "sources": [
    "fr_wik",
    "synonymo_fr",
    "antonymes_org"
  ],
  "phoneme": "/ʁəmɛd/",
  "conjugations": {}
}
```

Here are the specifications of each field :

- `synonyms` (`[]string`): List of synonyms
- `antonyms` (`[]string`): List of antonyms
- `etymologies` (`[]string`): List of etymologies
- `definitions` (`[]{}`): List of objects containing a word definition
    - `gender` (`string`): The gender of defined word
    - `nature` (`string`): The grammar class of defined word
    - `explanations` (`[]string`): List of possible explanation of defined word
    - `examples` (`[]string`): List of examples sentences using this word (NOT IMPLEMENTED)
- `plurals` (`[]{}`): The word plurals
  - `label`: A label related to the type of the plural
  - `singular`: The word as singular
  - `plural`: The plural of the word
- `source` (`string[]`): <a name="sourcesids"></a> A list of sources ids, to be displayed in interface. Their urls and link can be found at [app/src/functions/sources.ts](https://github.com/camarm-dev/remede/tree/main/app/src/functions/sources.ts). Sources are also described at [Database Credits](/docs/database/credits) page.
- `phoneme` (`string`): International Phonetic Alphabet pronunciation of the word
- `conjugations` (`{}`): Object containing word's conjugations
    - `[mode name]` (`{}`): Object containing conjugations' tenses for mode
        - `[tense name]` (`{}`): Object containing subjects of tense
            - `[subject]` (`string`): Verbal form (of `mode, tense, subject`)
