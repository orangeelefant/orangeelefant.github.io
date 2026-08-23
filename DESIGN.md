# DESIGN.md — orangeelefant.github.io

Ensidig visitkortssajt på GitHub Pages: Christoffer Holmgren, Webraketen och Rastahunden.
En fil, `index.html`, cirka 3,9 kB inklusive inlinad CSS och JSON-LD. Inget byggsteg,
ingen JavaScript, inga externa resurser.

Designen är medvetet minimal. Sidan finns för att vara en verifierbar identitetsnod i
schema-grafen och en läsbar landningsplats, inte för att sälja något. Allt som lägger till
en byggkedja eller en extern begäran hör inte hemma här.

## Tokens

Allt ligger inline i `<style>` i `index.html`. Det finns ingen tokenfil, och det ska inte
finnas en så länge sajten är en enda fil.

| Roll | Värde |
|---|---|
| Text | `#222` |
| Text, dämpad (`.lede`) | `#555` |
| Text, metadata (`.meta`) | `#888` |
| Länk | `#1a52e3` |
| Linjer (`h2`, `.meta`) | `#eee` |
| Bakgrund | webbläsarens standard, sätts inte |

## Typografi

Systemstacken, `-apple-system, system-ui, sans-serif`. Inga webbtypsnitt, eftersom en
extern typsnittsbegäran skulle vara sidans enda nätverksanrop utöver HTML:en.

| Element | Storlek | Övrigt |
|---|---|---|
| Brödtext | 16 px | `line-height: 1.6` |
| `h1` | 1,85 rem | |
| `h2` | 1,2 rem | understruken med 1 px `#eee`, `padding-bottom: .3em` |
| `.lede` | 1,1 rem | |
| `.meta` | 0,9 rem | överstruken med 1 px `#eee` |

## Layout

En centrerad kolumn, `max-width: 760px`, `padding: 32px 24px`. Ingen media query behövs:
kolumnen krymper med visningsytan och `viewport`-taggen sköter resten.

Vertikal rytm sätts av `h2` med `margin: 1.6em 0 .5em` och listposter med `margin: .5em 0`.

## Strukturerad data

`index.html` innehåller en JSON-LD-graf med `WebSite` och `ProfilePage` som pekar på samma
`#person`. Det är sidans egentliga funktion i portföljen: en stabil, verifierad
identitetsreferens som övriga sajters scheman kan länka till. Ändrar du namn, roll eller
länkar i grafen, kontrollera att inget annat repo pekar på ett fält du tagit bort.

## Gränser

- Ingen build, inget `package.json`, inga beroenden.
- Inga externa resurser: inga typsnitt, inga bilder från CDN, ingen analys.
- Håll filen under cirka 5 kB. Behöver sidan mer än så är det ett tecken på att innehållet
  hör hemma på webraketen.se i stället.
