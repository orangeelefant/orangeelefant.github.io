---
version: alpha
name: orangeelefant.github.io
description: Ensidig visitkortssajt på GitHub Pages. Värdena speglar den inlinade <style> i index.html; det finns ingen annan tokenkälla.
colors:
  primary: "#1a52e3"   # länk (a)
  text: "#222"         # body
  muted: "#555"        # .lede
  meta: "#888"         # .meta
  rule: "#eee"         # linjer under h2 och över .meta
  bg: "#ffffff"        # webbläsarens standard, sätts inte i CSS
typography:
  body:
    fontFamily: "-apple-system, system-ui, sans-serif"
    fontSize: 16px
    lineHeight: 1.6
  h1:
    fontFamily: "-apple-system, system-ui, sans-serif"
    fontSize: 1.85rem
  h2:
    fontFamily: "-apple-system, system-ui, sans-serif"
    fontSize: 1.2rem
  lede:
    fontFamily: "-apple-system, system-ui, sans-serif"
    fontSize: 1.1rem
  meta:
    fontFamily: "-apple-system, system-ui, sans-serif"
    fontSize: 0.9rem
rounded:
  none: "0px"
spacing:
  page-y: 32px
  page-x: 24px
  container: 760px
  list-indent: 1.2em
components:
  page:
    backgroundColor: "{colors.bg}"
    textColor: "{colors.text}"
    typography: "{typography.body}"
    padding: "32px 24px"
    width: 760px
  link:
    textColor: "{colors.primary}"
  heading-section:
    textColor: "{colors.text}"
    typography: "{typography.h2}"
    padding: "0 0 0.3em"
  lede:
    textColor: "{colors.muted}"
    typography: "{typography.lede}"
  meta:
    textColor: "{colors.meta}"
    typography: "{typography.meta}"
    padding: "1em 0 0"
---

# orangeelefant.github.io: designsystem

Ensidig visitkortssajt på GitHub Pages: Christoffer Holmgren, Webraketen och Rastahunden.
En fil, `index.html`, cirka 3,9 kB inklusive inlinad CSS och JSON-LD. Inget byggsteg,
ingen JavaScript, inga externa resurser. Allt ligger inline i `<style>` i `index.html`;
ändras CSS:en där ska den här filen ändras i samma commit.

## Overview

Designen är medvetet minimal. Sidan finns för att vara en verifierbar identitetsnod i
schema-grafen och en läsbar landningsplats, inte för att sälja något. Allt som lägger till
en byggkedja eller en extern begäran hör inte hemma här.

## Design Principles

- Ingen build, inget `package.json`, inga beroenden.
- Inga externa resurser: inga typsnitt, inga bilder från CDN, ingen analys.
- Ingen tokenfil så länge sajten är en enda fil. Tokens ovan är dokumentation, inte kod.
- Håll filen under cirka 5 kB. Behöver sidan mer än så är det ett tecken på att innehållet
  hör hemma på webraketen.se i stället.

## Color

| Roll | Token | Värde |
|---|---|---|
| Text | `text` | `#222` |
| Text, dämpad (`.lede`) | `muted` | `#555` |
| Text, metadata (`.meta`) | `meta` | `#888` |
| Länk | `primary` | `#1a52e3` |
| Linjer (`h2`, `.meta`) | `rule` | `#eee` |
| Bakgrund | `bg` | webbläsarens standard, sätts inte |

`bg` står i tokens bara för att kontrastberäkningen ska ha något att räkna mot. Lägg inte
till en `background` i CSS:en för den skull.

## Typography

Systemstacken, `-apple-system, system-ui, sans-serif`. Inga webbtypsnitt, eftersom en
extern typsnittsbegäran skulle vara sidans enda nätverksanrop utöver HTML:en.

| Element | Storlek | Övrigt |
|---|---|---|
| Brödtext | 16 px | `line-height: 1.6` |
| `h1` | 1,85 rem | |
| `h2` | 1,2 rem | understruken med 1 px `#eee`, `padding-bottom: .3em` |
| `.lede` | 1,1 rem | |
| `.meta` | 0,9 rem | överstruken med 1 px `#eee` |

## Spacing & Layout

En centrerad kolumn, `max-width: 760px`, `padding: 32px 24px`. Ingen media query behövs:
kolumnen krymper med visningsytan och `viewport`-taggen sköter resten.

Vertikal rytm sätts av `h2` med `margin: 1.6em 0 .5em` och listposter med `margin: .5em 0`.
`.lede` har `margin: .4em 0 1em`, `.meta` har `margin-top: 3em` och `padding-top: 1em`.
Listor dras in med `padding-left: 1.2em`. En global reset (`*{box-sizing:border-box;
margin:0;padding:0}`) nollställer allt annat.

## Components

- **h2 (sektionsrubrik):** 1,2 rem, 1 px `#eee` under, `padding-bottom: .3em`.
- **.lede:** ingress direkt under `h1`, `#555`, 1,1 rem.
- **.meta:** sidfot med GitHub-länkar, `#888`, 0,9 rem, 1 px `#eee` över.
- **Länkar:** `#1a52e3`, webbläsarens standardunderstrykning.

### Strukturerad data

`index.html` innehåller en JSON-LD-graf med `WebSite` och `ProfilePage` som pekar på samma
`#person`. Det är sidans egentliga funktion i portföljen: en stabil, verifierad
identitetsreferens som övriga sajters scheman kan länka till. Ändrar du namn, roll eller
länkar i grafen, kontrollera att inget annat repo pekar på ett fält du tagit bort.

## Accessibility

Text `#222` och länkar `#1a52e3` mot vit bakgrund klarar WCAG AA med god marginal, liksom
`.lede` (`#555`). `.meta` (`#888` mot vitt) ligger under 4,5:1 och är bara godtagbar för att
den är sekundär sidfotstext; använd den inte för något viktigt. Länkar skiljs från brödtext
med understrykning, inte bara färg.
