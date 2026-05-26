# Ansala Siberians — Sprievodca úpravou webu

## Štruktúra súborov

```
ansala/
├── index.html          ← Hlavná stránka (SLOVENČINA)
├── en/
│   └── index.html      ← Anglická verzia
├── css/
│   └── style.css       ← Všetky štýly (farby, písmo, rozloženie)
├── images/             ← VLOŽ SEM VŠETKY FOTOGRAFIE
│   ├── hero-husky.jpg
│   ├── aurora.jpg
│   ├── thor.jpg
│   └── news-*.jpg
└── README.md           ← Tento súbor
```

---

## Ako vložiť fotografie

Krok 1: Vlož fotografiu do priečinka `images/`
Krok 2: V HTML nájdi komentár ako `<!-- <img src="images/hero-husky.jpg" ...> -->`
Krok 3: Odkomentuj ho (odmaž `<!--` a `-->`) a zober priľahlý `<div class="...-placeholder">...</div>`

---

## Kde upraviť texty (SK verzia — index.html)

| Čo hľadám | Kód alebo text na vyhľadanie |
|-----------|------------------------------|
| Hlavný nadpis hero | "Chov s vášňou, láskou a srdcom" |
| Popis webu | "Vitajte v Ansala Siberians" |
| História stanice | "Chovateľská stanica Ansala Siberians pôsobí" |
| Email | "info@ansala-siberians.sk" |
| Telefón | "+421 900 000 000" |
| Instagram URL | "https://instagram.com/ansala.siberians" |
| Rok v footeri | "© 2025 Ansala Siberians" |

---

## Ako pridať nového psa

V `index.html` nájdi komentár `PROFIL PSA #2` a skopíruj celý blok `<div class="dog-profile">...</div>` za neho. Uprav meno, tituly a detaily.

## Ako pridať novinku

V `index.html` nájdi sekciu `NOVINKY` a skopíruj blok `<div class="news-card">...</div>`. Zmeň emoji placeholder, dátum, nadpis a text.

## Ako pridať vrh

V `index.html` nájdi sekciu `ŠTENIATKA` a skopíruj blok `<div class="litter-card">...</div>` do správnej záložky (aktuálne / plánované).

---

## Farby — ako zmeniť

V súbore `css/style.css` nájdi sekciu `:root {` na začiatku. Premenné:

```css
--color-primary:      #b8a9d0;   /* pastelová fialová */
--color-primary-dark: #8b78b2;   /* tmavšia fialová (tlačidlá, linky) */
--color-primary-light:#e8e0f5;   /* veľmi svetlá fialová (pozadie sekcií) */
```

---

## Nasadenie na GitHub Pages

1. Vytvor repozitár na github.com (napr. `ansala-siberians`)
2. Nahraj všetky súbory (drag & drop cez GitHub web alebo cez Git)
3. Choď do Settings → Pages → Source: "Deploy from a branch" → branch: `main`, folder: `/ (root)`
4. Web bude dostupný na `https://tvoje-meno.github.io/ansala-siberians/`

## Nasadenie na Netlify (odporúčané — jednoduchšie)

1. Choď na netlify.com a vytvor účet
2. Klikni "Add new site" → "Deploy manually"
3. Pretiahni celý priečinok `ansala/` do prehliadača
4. Netlify ti automaticky vygeneruje URL

## Funkčný kontaktný formulár (Formspree — bezplatný)

1. Zaregistruj sa na formspree.io
2. Vytvor nový formulár, dostaneš kód tvaru `https://formspree.io/f/xxxxxabc`
3. V `index.html` aj `en/index.html` nájdi `<form action="#">` a zmeň `#` na tvoj endpoint
