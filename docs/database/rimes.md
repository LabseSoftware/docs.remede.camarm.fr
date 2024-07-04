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

Remède is able to serve a **rhymes dictionary** using its database.

It uses the field **phoneme** to know which words ends with the same sound. The query looks like (with phoneme `e`)
```SQL
SELECT * FROM dictionary WHERE phoneme LIKE '%e'
```

TODO: more precision with elide ect