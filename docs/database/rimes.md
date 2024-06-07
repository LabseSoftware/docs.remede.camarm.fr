---
layout: default
title: Rimes
parent: Database
permalink: /docs/database/rimes
---

# Rimes database
Discover how the rimes database work. 
{: .fs-6 .fw-300 }

## How it work ?

Remède uses a project called [drime](https://a3nm.net/git/drime) (2011-2020 by Antoine Amarilli, [GPL-v3](https://a3nm.net/git/drime/file/COPYING.html)) to generate a french rimes 
database dump, and add this database to the main one using the script `scripts/build_rimes.py`.

### Build the database

We provide a version of `drime.sql` but you can build your own one with the instruction on [drime's README](https://a3nm.net/git/drime/README)

To integrate this database in Remède database, you must execute `scripts/build_rimes.py`.

## Rimes service

The rime database (drime one) is pushed into `data/remede.db` (in a table named `rimes`) with the script `scripts/build_rimes.py`.

When the database is downloaded in the mobile application, the "Rimes" menu link is unlocked.

