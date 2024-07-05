---
layout: default
title: Database schema
parent: Database
permalink: /docs/database/db-schema
nav_order: 3
---

# Database schema
Discover how Remède's database is storing an entire dictionary. 
{: .fs-6 .fw-300 }

Remède database is an **Sqlite 3** database.

## Tables

The database only hav one table :

| Name       | Description                                                                |
|------------|----------------------------------------------------------------------------|
| dictionary | all Remède [documents](https://docs.remede.camarm.fr/docs/database/schema) |

## Dictionary table

The unique table of Remède contains the following fields:

| Field     | Description                                                                               | Type      | Example                                       |
|-----------|-------------------------------------------------------------------------------------------|-----------|-----------------------------------------------|
| word      | The word                                                                                  | `string`  | `manger`                                      |
| indexed   | The word but case, accent and special chars insensitive                                   | `string`  | `manger` (`a vue d oeil` is a better example) |
| phoneme   | The word's phoneme                                                                        | `string`  | `m#Ze`                                        |
| nature    | The word's nature                                                                         | `string`  | `VER\|manger`                                 |
| syllables | The word's syllables number                                                               | `integer` | `2`                                           |
| elidable  | Can the word be precede by an "élide"^1                                                   | `boolean` | `false` or `null` if no data                  |
| feminine  | Is the last phoneme "féminine"                                                            | `boolean` | `false` or `null` if no data                  |
| document  | The word's [document](https://docs.remede.camarm.fr/docs/database/schema), as JSON-string | `string`  | `{...}`                                       |


- See [Rimes](https://docs.remede.camarm.fr/docs/database/rimes) to know how this is used as a rhymes dictionary

----
[^1]: In French, syllables can variate in pronunciation (e.g. the "l'" determinant is placed before the word, at pronunciation on syllable will be canceled).
