---
layout: default
title: Contributing
nav_order: 12
permalink: /docs/contributing
---

# Contributing
Learn how to contribute to Remède !
{: .fs-6 .fw-300 }

## How to contribute
**To contribute, you can:**
- Open an issue ([here](https://github.com/camarm-dev/remede/issues/new/choose))
- Choose an issue, fork the repository, resolve it and open a pull request ! ([complete guide](#guide))
- Contact us to become part of our team (software@camarm.dev)
    - So you'll have access to this repository

## Guide
1. Open or choose an issue on our [issue page](https://github.com/camarm-dev/remede/issues)
2. Fork and clone the repository on your computer
3. Read [the documentation](https://docs.remede.camarm.fr), and contact us for more informations (at software@camarm.dev).
4. Make your changes, and separate your work in multiple commits
5. Open a pull request
6. Wait and make requested changes
7. You're now a contributor ! Thank you very much !

## Add words

Remède fetches words from the Wictionary but sometimes, words are not in our list so, you can add custom words...

1. Add it to `data/IPA.txt`
   1.  In alphabetic order, add your word with the following schema `word\t/phonetic/` (`\t` represents a <kbd>TAB</kbd> char, not spaces)
2. Add it to `data/custom_words.json`, if necessary
   1. Check on the [french Wictionary](https://fr.wiktionary.org) if your word exist.
   2. If it does not exist, fill his document manually in the `data/custom_words.json`. Don't forget to quote your sources in the `credits` field.
3. Before making a PR, rebuild ressources (so your word will be added next time database is built)
   1. Run `python3 scripts/pre_generate_ressources.py`, if it outputs an error, check the previous steps...

Check also [Building database - About - Quickly add a word](https://docs.remede.camarm.fr/docs/database/build/about#quickly-add-a-word)

## Add cheatsheets

Remède needs contributors who can add cheatsheets !

You can find a documentation about writting cheatsheets [here](https://docs.remede.camarm.fr/docs/cheatsheets)

## More

You can browse the documentation on the left-side menu.
Do not hesitate to contact me us at [software@camarm.dev](mailto:software@camarm.dev) for more information.
