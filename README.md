# Blog Posts Example

Ovaj folder pokazuje kako treba da izgledaju blog postovi za Vet Record.

## Struktura

```
posts/
├── pet-vaccination-guide.md
├── medication-reminders-tips.md
└── senior-pet-care-checklist.md
```

## Frontmatter (obavezno na početku svakog fajla)

Svaki post mora da ima YAML frontmatter između `---`:

```yaml
---
title: Naslov članka
description: Kratak opis za SEO i prikaz na listi (1-2 rečenice)
date: 2025-01-15
image: ime-slike.jpg
author: Ime autora
---
```

| Polje       | Obavezno | Opis |
|-------------|----------|------|
| `title`     | Da       | Naslov članka |
| `description` | Preporučeno | SEO opis, prikazuje se na kartici |
| `date`     | Preporučeno | Datum objave (YYYY-MM-DD) |
| `image`    | Ne       | Slika za karticu/hero (relativna putanja) |
| `author`   | Ne       | Ime autora |

## Slike

- **U frontmatter-u:** `image: hero.jpg` – slika mora biti u istom folderu kao `.md` fajl
- **U sadržaju:** `![Alt text](./slika.jpg)` – relativna putanja od fajla posta

Slike mogu biti u:
- istom folderu kao post
- podfolderu npr. `./images/hero.jpg`

## Markdown podrška

- **Naslovi:** `#`, `##`, `###`
- **Bold:** `**tekst**`
- **Italic:** `*tekst*`
- **Liste:** `-` ili `1.`
- **Citati:** `>`
- **Linkovi:** `[tekst](url)`
- **Slike:** `![alt](url)`

## Kako koristiti

1. Kopiraj ovaj `posts` folder u svoj GitHub repo
2. Postavi `BLOG_GITHUB_REPO_URL=owner/repo` u `.env.local`
3. Postavi `BLOG_GITHUB_POSTS_PATH=posts` (ako koristiš drugi naziv foldera)
4. Dodaj nove `.md` ili `.mdx` fajlove u `posts/` folder

## Primer minimalnog posta

```markdown
---
title: Moj prvi post
description: Kratak opis
date: 2025-02-01
---

Sadržaj članka ovde...
```
