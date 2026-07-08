# TechnoVolley '26 — Prijava na turnir

Enostavna spletna stran za prijavo ekip na odbojkarski turnir (Planet Circle).
Vse je v enem samem `index.html` — brez strežnika, brez baze. Oddane prijave prek
[Formspree](https://formspree.io) pridejo naravnost na tvojo e‑pošto.

## Kako pognati

Samo odpri `index.html` v brskalniku (dvojni klik) — ali za lokalni strežnik:

```bash
python3 -m http.server 8000
# odpri http://localhost:8000
```

## Kaj urediti vsako leto

Na vrhu `<script>` bloka v `index.html` je objekt `CONFIG` — spremeni samo te vrstice:

| Polje | Pomen |
|-------|-------|
| `eventDateISO` | datum + ura turnirja (poganja odštevalnik) |
| `dateLabel`    | prikazani datum |
| `location`     | lokacija |
| `fee`          | prijavnina |
| `instagram`    | povezava na Instagram |
| `formspree`    | tvoj Formspree endpoint (kamor pridejo prijave) |
| `avatarUrl`    | profilna slika v glavi |

## Formspree

Prijave gredo na endpoint iz `CONFIG.formspree` (trenutno `mblynnep` iz lani).
Za ločeno zbiranje prijav 2026 lahko ustvariš nov obrazec na formspree.io in
zamenjaš samo to eno vrstico.

## Deploy

Ker je stran statična, jo lahko brezplačno gostiš na **GitHub Pages**, **Netlify**
ali **Vercel** — samo naloži `index.html`.
