
---
layout: default
title: Writing sheets
parent: Database
nav_order: 10
permalink: /docs/sheets
---

# French sheets
Remède can give you french lessons !
{: .fs-6 .fw-300 }

{: .warning-title }
> Remède needs you
>
> Remède does not have enough french Sheets... You can add ones to help us !

Sheets are readable inside the application. They are a resume of french grammar, conjugate ect...


## Writing a sheet

Sheet containing french orthography and grammar lessons are written in the `data/fiches` folder.

They are written in `markdown` and use `front-matter` to work.

Sheet example:

```markdown
---
nom: Exemple de fiche
description: Ceci est la première fiche
credits: https://remede.camarm.fr/sheets-credits#example
slug: exemple
tags: 
  - grammaire
  - orthographe
---

# Exemple

Ceci est un exemple de fiche.
```

Available tags: `grammaire`, `orthographe`, `conjugaison`, `lexique`, `style`, `typographie`

To credit and permit right attribution of these sheets, please **fill correctly** the `credits` fields in the frontmatter.
- `credits.url`: Source URL (Remède GitHub link or source website url)
- `credits.attributions`: The person or project to attribute
- `credits.text`: The ressources that helped you, the file modification historic.

Please fill correctly this file, because it tracks authors and contributions, and is here to respect privacy policies and copyrights about Rèmede and the sources of its data ! 
