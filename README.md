# horisontell-scroll-flashback

Status: active

En fristående HTML-sida som återskapar ett Flashback-trådinlägg om
**Pi-dagen** — med kodrutor som visar olika sätt att hantera lång,
horisontellt rinnande kod.

## Features

- **Flashback-look** — rubrik, citatrutor, signatur och inläggsmeta i forumstil.
- **Horisontell scroll i kodrutor** — kodblocken visas i tre lägen via
  `data-mode` på inläggswrappern: `wrap` (mjuk radbrytning), `overflow`
  (hård brytning på tecken) och `native` (horisontell scroll).
- **Helt fristående** — `index.html` packar upp sina egna inbäddade,
  komprimerade resurser i webbläsaren. Inga externa beroenden, inget byggsteg.

## Getting started

```sh
git clone https://github.com/GeGGe01/horisontell-scroll-flashback.git
cd horisontell-scroll-flashback
xdg-open index.html        # eller: python3 -m http.server 8000
```

JavaScript måste vara aktiverat — sidan bygger upp sitt innehåll vid inläsning.

## License

[CC0 1.0 Universal](LICENSE) — public domain.
