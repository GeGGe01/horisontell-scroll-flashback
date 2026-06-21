# horisontell-scroll-flashback

Status: active

En statisk sida som återskapar Flashback-inlägget **"Pi-dagen idag!"**
(sp95149773) — med en växlare mellan mobil-/datorwebb och flera exempel på
hur kodrutor hanterar lång, horisontellt rinnande kod.

## Features

- **Flashback-look** i både mobil- och datorvy, med växlare i en kontrollrad.
- **Kodrute-lägen** styrda av `data-mode` på inläggswrappern:
  - Mobil: `wrap` (radbrytning), `hscroll` (horisontell scroll),
    `hvscroll` (+ vertikal scroll vid ≥30 rader).
  - Dator: `native` (allt ryms), `overflow` (medvetet trasig),
    `drag` (horisontell scroll med grab-and-drag).

## Files

- `index.html` — hela designen (markup + logik). Entry point.
- `support.js` — runtime som `index.html` laddar via `<script src>`. Krävs.
- `assets/avatar-thecrash.jpg` — avatar.

## Getting started

Servera mappen statiskt (relativa sökvägar till `support.js` och `assets/`):

```sh
npx serve .        # öppna sedan /index.html
```

`support.js` hämtar React + Babel från unpkg vid inläsning, så en
nätverksanslutning krävs första gången.

## License

[CC0 1.0 Universal](LICENSE) — public domain.
