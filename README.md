# FORMULA — Vulkanizer (sajt)

High-converting jednostranični sajt za vulkanizersku radnju **FORMULA** u Beogradu.
Statički sajt (HTML/CSS/JS) — bez build koraka, spreman za **GitHub Pages**.

---

## ⚠️ PRE SLANJA KLIJENTU — popuni prave podatke

Sajt je napravljen kao demo. Zameni sledeće placeholdere pravim podacima:

| Šta | Gde u kodu | Trenutno (placeholder) |
|-----|-----------|------------------------|
| **Telefon** | ✅ uneto: **065 880-6122** (`tel:+381658806122`) | gotovo |
| **Adresa** | ✅ uneto: **Mokroluška 82, 11010 Beograd** | gotovo |
| **Ocena** | ✅ uneto: **4,9 ★ / 121 recenzija** (Google) | gotovo |
| **Radno vreme** | ⚠️ `index.html` — tabela `.hours` | **placeholder** 08–19 / Sub 08–15 — POTVRDI |
| **Recenzije (tekst)** | `index.html` — sekcija `#recenzije` | ilustrativne (zameni Google recenzijama) |
| **Statistika (15 min, 20+ god)** | `index.html` — `.hero-stats` | potvrdi tačne brojeve |
| **Mapa** | `index.html` — `iframe` koordinate `44.7779024,20.4969406` | proveri da pokazuje tačnu lokaciju |

> Jedino još fali **radno vreme** — ako se razlikuje od placeholdera, otvori `index.html`,
> nađi tabelu `.hours` (sekcija `#lokacija`) i izmeni sate. Telefon, adresa i ocena su uneti.

---

## Lokalno pokretanje

Samo otvori `index.html` u browseru. Ili pokreni mini server:

```bash
python -m http.server 8000
# pa otvori http://localhost:8000
```

## Deploy na GitHub Pages

1. Napravi novi repo na GitHub-u (npr. `formula-vulkanizer`).
2. Push-uj sadržaj ovog foldera u `main` granu.
3. **Settings → Pages → Source: `main` / root** → Save.
4. Sajt je živ na `https://<korisnik>.github.io/formula-vulkanizer/` za par minuta.

Fajl `.nojekyll` je već uključen (sprečava Jekyll obradu).

---

## Struktura

```
formula-vulkanizer/
├── index.html        # ceo sadržaj sajta
├── styles.css        # dizajn (motorsport, tamna tema, F1-crveni akcenat)
├── script.js         # reveal animacije, brojači, mobilni meni
├── assets/favicon.svg
├── .nojekyll
└── README.md
```

## Dizajn
- **Identitet:** motorsport — tamna podloga `#0a0a0b`, jedan crveni akcenat (`#e10600`), tehnička monospace tipografija.
- **Font:** Archivo (naslovi), Inter (tekst), JetBrains Mono (brojevi) — preko Google Fonts.
- Potpuno responzivan, lepljivo „Pozovi" dugme na mobilnom, poštuje `prefers-reduced-motion`.
