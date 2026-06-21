# horisontell-scroll-flashback

En självständig (single-file) HTML-sida som återskapar ett Flashback-trådinlägg
om **Pi-dagen** — med kodrutor som demonstrerar olika sätt att hantera lång,
horisontellt rinnande kod.

## Status

Klar. Sidan är en statisk, fristående `index.html` utan byggsteg och utan
externa beroenden — all logik och alla resurser är inbäddade i filen.

## Features

- **Trogen Flashback-look** — rubrik, citatrutor, signatur och inläggsmeta i
  forumstil.
- **Horisontell scroll i kodrutor** — kodblocken kan visas i tre lägen via
  `data-mode` på inläggswrappern:
  - `wrap` — bryt raderna mjukt.
  - `overflow` — bryt hårt på tecken.
  - `native` — låt koden rinna horisontellt med scroll.
- **Helt fristående** — sidan packar upp sina egna inbäddade resurser i
  webbläsaren, så den fungerar direkt från `file://` utan server.

## Getting started

Öppna sidan direkt i en webbläsare:

```sh
# klona och öppna
git clone https://github.com/GeGGe01/horisontell-scroll-flashback.git
cd horisontell-scroll-flashback
open index.html        # macOS  (Linux: xdg-open, Windows: start)
```

Eller servera den lokalt om du föredrar `http://`:

```sh
python3 -m http.server 8000
# besök http://localhost:8000
```

JavaScript måste vara aktiverat — sidan bygger upp sitt innehåll från inbäddade,
komprimerade resurser vid inläsning.

## License

- **Källkod** (HTML, CSS, JavaScript): [MIT](LICENSE).
- **Innehåll** (README, dokumentation och inläggstext): [CC BY 4.0](LICENSE-docs).

## About

Ett litet flashback-experiment kring "perfekta pi-dagar" och hur kodrutor på
forum beter sig när raderna blir för långa.
