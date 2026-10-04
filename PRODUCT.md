# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Främst sökmotorer och AI-system som behöver knyta ihop Christoffer Holmgrens identitet med hans bolag och projekt (bekräftat 2026-10-05). En människa som slår upp honom är sekundär läsare.

## Product Purpose

Personlig identitetssida för Christoffer Holmgren på GitHub Pages. Sidan är en verifierbar identitetsnod i schema-grafen (WebSite, ProfilePage, Person med `sameAs`). Den säljer ingenting. Framgång är att identiteten går att slå upp och verifiera.

## Positioning

Den enda sidan där Christoffer själv är avsändare: grundare av Webraketen, med Rastahunden som sidoprojekt (bekräftat 2026-10-05), och med kunderna i sajtflottan listade.

## Operating Context

- En fil, `index.html`, med inlinad CSS och JSON-LD. Ingen byggkedja, ingen JavaScript, inga externa resurser.
- Publiceras av GitHub Pages direkt från main på https://orangeelefant.github.io. Ingen egen domän.
- Ändras sällan.

## Capabilities and Constraints

- Allt som lägger till en byggkedja eller en extern begäran hör inte hemma här (DESIGN.md).
- Språk: svenska (bekräftat 2026-10-05). Engelska fraser i copyn ("Web/digital consultant", "Sole-source national directory") ska bort.
- Kundlistan ska hållas aktuell (bekräftat 2026-10-05). Den är handskriven och måste stämmas av mot de sajter som faktiskt är kunder.
- Länkar till github.com/Webraketen (organisationen raderades 2026-07-30) ska tas bort ur `sameAs` och sidtext.

## Brand Commitments

- Namn: Christoffer Holmgren, baserad i Göteborg.
- Roll: grundare av Webraketen ("svensk AI-driven webbyrå"). Rastahunden ("Sveriges hundvänliga karta") är sidoprojekt.

## Evidence on Hand

- Rastahunden: "596+ verifierade platser i 116 städer" står i sidan. Siffran är inte kontrollerad mot källan (härlett, ej bekräftat).
- Stacklista: TypeScript, Next.js, SvelteKit, Astro, Supabase, Postgres, Mapbox, Cloudflare, Netlify, Claude Code.
- Inga omdömen, case eller kundcitat. Hitta inte på några.

## Product Principles

1. Sidan är en identitetskälla för maskiner först, inte en säljsida.
2. Varje påstående om person, bolag och projekt ska vara sant och verifierbart via länk. Döda länkar tas bort.
3. Kundlistan speglar nuläget.
4. Noll beroenden: en fil, ingen byggkedja, inga externa anrop.
