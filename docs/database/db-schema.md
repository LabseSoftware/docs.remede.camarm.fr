---
layout: default
title: Database schema
parent: Database
---

# Database schema
Discover how Remède's database is storing an entire dictionary. 
{: .fs-6 .fw-300 }

## Tables

The database is divided in three tables :

| Name       | Description                                        |
|------------|----------------------------------------------------|
| dictionary | all Remède [documents][Document schema]            |
| rimes      | an indexations of words to make a rimes dictionary |
| wordlist   | an index of all the words to make search faster    |

## Dictionary table

This table contains rows with the following fields:

| Field    | Description                                            | Type     |
|----------|--------------------------------------------------------|----------|
| word     | The word                                               | `string` |
| document | The word's [document][Document Schema], as JSON-string | `string` |


## Rimes table

This table contains rows with the following fields:

| Field    | Description                             | Type      | Example       |
|----------|-----------------------------------------|-----------|---------------|
| word     | The word                                | `string`  | `manger`      |
| phon     | The word's phoneme                      | `string`  | `m#Ze`        |
| orgi     | The word's nature                       | `string`  | `VER\|manger` |
| freq     | The word's frequency in french language | `float`   | `37905`       |
| min_nsyl | The word's maximum syllables^1          | `integer` | `2`           |
| max_nsyl | The word's minimum syllables^1          | `integer` | `2`           |
| word_end | The word's last syllables               | `string`  | `er`          |
| phon_end | The word's last phoneme                 | `string`  | `e`           |
| elidable | Can the word be precede by an "élide"^1 | `boolean` | `false`       |
| feminine | Is the last phoneme "féminine"          | `boolean` | `false`       |

See [Rimes][Rimes]

## Wordlist table

This table contains rows with the following fields:

| Field   | Description                                             | Type     | Example        |
|---------|---------------------------------------------------------|----------|----------------|
| word    | The word                                                | `string` | `à vue d'œil`  |
| indexed | The word but case, accent and special chars insensitive | `string` | `a vue d oeil` |

[^1] In French, syllables can variate in pronunciation (e.g. the "l'" determinant is placed before the word, at pronunciation on syllable will be canceled).
