---
layout: default
title: Translation
nav_order: 10
permalink: /docs/translation
---

# Translation
Remède is translated in multiple languages ! Let's learn how to translate Remède !
{: .fs-6 .fw-300 }

Remède has introduced a **translation system** since `1.3.0`. Remède uses **[i18n](https://vue-i18n.intlify.dev/)** for Vue as a translation system.

## Translating

The translations by languages are inside the `app/src/data/translations/[locale].json`.

For example, `en.json` (section "home")
```json
{
    "home": {
        "wordOfDay": "Word of day",
        "randomWord": "Random word",
        "myBookmarks": "My bookmarks",
        "forYou": "For you",
        "seeAll": "See all",
        "askToAddAWord": "Ask to add a word",
        "report": "Report",
        "searchWord": "Search a word...",
        "changelog": "Changelog"
    }
}
```
You can see that there are multiple translation in english.

## Add a language

1. Add his `app/src/data/translations/[locale].json` file
2. Define it in `app/src/i18n.ts`

```typescript
import yourNewLanguageTranslations from "@/data/translations/en.json"

const globalizationList = {
    fr: frenchTranslations,
    en: englishTranslations,
    yourLocale: yourNewLanguageTranslations
}

```

3. Define your language name in `app/src/functions/locales.ts`

```typescript
const locales = {
    en: "English",
    fr: "Français",
    yourLocale: "New language",
    dialects: {
        en: [
            "en-GB",
            "en-US",
            "en-CA",
            "en-AU",
            "en-NZ"
        ]
    }
} 
```

If your language has specific dialects for the correction service, add its dialects... See [Languagetool API documentation](https://languagetool.org/http-api/swagger-ui/#!/default/post_check), the field "language" in the check function.

And you're done !

## And about the database ?

Remède serve a **French database**, but we are working on internationalization of the database.

**How it works ?**
We re-use as many code as possible across generation scripts and uses different scrapping services to build our databases.

To serve multiple databases, we define it inside `server.py`

```python

@app.get('/')
def root():
    return {
        "version": version,
        "message": "Check /docs for documentation",
        "dataset": DATASET,
        "hash": DATASET,
        "total": entities,
        "dictionnaires": {
            # Default dictionary
            "remede": {
                "nom": "Remède (FR) ~500Mb",
                "slug": "remede",
                "hash": DATASET
            },
            # Wow ! We are just serving a new dictionary
            "remede.en": {
                "nom": "Remède (EN)"
                 ...
            }
        }
    }
```

See [Database Internationalization](/docs/database/internationalization) docs for more information about a specific language.
