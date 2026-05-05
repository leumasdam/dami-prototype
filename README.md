# DAMI Pracovné Odevy — Redesign Prototype

Live: https://leumasdam.github.io/dami-prototype/
Repo: https://github.com/leumasdam/dami-prototype

---

## Čo je toto

High-fidelity interaktívny prototyp redesignu e-shopu dami-pracovne-odevy.sk.
Postavený ako single-file HTML (index.html) s inline CSS a JS. Žiadne závislosti okrem
Google Fonts (Inter). Funguje offline aj online.

---

## Prečo bol redesign potrebný (UX audit)

Pôvodný web mal tieto CRO problémy:

1. Žiadna hodnota above the fold — žiadna headline, žiadne USP
2. Kognitívna záťaž — 9 hlavných kategórií bez segmentácie zákazníka
3. Žiadne trust signály — gmail adresa, žiadne recenzie, žiadne záruky
4. Slabé filtre — len kategórie, žiadna farba/veľkosť/cena
5. Product card bez quick-add, bez výberu veľkosti
6. Žiadna segmentácia — kuchár a stavbár servírovaní rovnako
7. Žiadny lead capture — žiadny newsletter, žiadna zľava

---

## Čo prototyp obsahuje

### Sekcie (zhora nadol)

  NAVBAR
  - Sticky s blur efektom pri scrollovaní
  - Logo + kategórie + telefón + cart s badge

  HERO
  - Split layout: text vľavo, foto vpravo
  - Fotka: profesionálny tím kuchárov (dami-hero-bg.jpg)
  - Gradient overlay: navy vlavo (text), amber/meď tint vpravo (psychológia apetítu)
  - 3 klikateľné segment karty: Gastro / Pracovné / Obuv
    → kliknutie scrolluje na produkty a automaticky filtruje
  - Floating UI karty: hodnotenie, doprava, objednávky, potvrdenie

  TRUST BAR
  - 4 stĺpce s animovanými počítadlami (IntersectionObserver)
  - 30+ rokov, 10 000+ zákazníkov, doprava zadarmo, 14 dní vrátenie

  PRODUKTY
  - Filter pills: Všetky / Gastro / Pracovné / Obuv
  - 8 produktových kariet s:
    → hover quick-add button (slide-up)
    → výber farby (swatche)
    → výber veľkosti (chipy)
    → stock indikátor (zelený/amber)
    → hodnotenia a počty recenzií
    → sale/new/top/dami badges

  KATEGÓRIE
  - 6 vizuálnych kariet s hover efektom a šípkou

  DAMI VÝROBA
  - Tmavá sekcia s USP (vlastná výroba 30 rokov)
  - 4 mini produktové karty

  B2B FORMULÁR
  - Cenová ponuka pre firmy
  - 4 benefity: zľavy, potlač, fakturácia, konzultant
  - Formulár s success state animáciou

  NEWSLETTER
  - Zľava 5% na prvý nákup
  - Email capture

  FOOTER
  - 4 stĺpce, kontakty, IBAN, otváracie hodiny

---

## Farebná paleta

  --orange:      #F97316   (CTA, akcentová — apetít, energia)
  --orange-dark: #EA580C   (hover stav)
  --navy:        #0F172A   (pozadie, profesionalita)
  --navy-2:      #1E293B
  --navy-3:      #334155
  --green:       #10B981   (skladom, success)
  --red:         #EF4444   (akcia, vypredaj)
  --amber:       #F59E0B   (hviezdy, posledné kusy)
  --muted:       #64748B   (sekundárny text)
  --border:      #E2E8F0

Hero overlay farby (psychológia):
  rgba(180,83,9)  — teplá meď/amber = teplo kuchyne, remeselnosť
  rgba(146,64,14) — tmavá meď = prémiová gastro estetika

---

## Súborová štruktúra

  dami-prototype/
  ├── index.html        ← celý prototyp (HTML + CSS + JS)
  ├── dami-hero-bg.jpg  ← hero fotka (tím kuchárov)
  └── README.md         ← tento súbor

---

## Ako spustiť lokálne

  # Stiahnuť repo
  git clone https://github.com/leumasdam/dami-prototype.git
  cd dami-prototype

  # Otvoriť v prehliadači
  open index.html           # macOS
  start index.html          # Windows
  xdg-open index.html       # Linux

  # Alebo spustiť lokálny server
  python3 -m http.server 8000
  # → http://localhost:8000

---

## Ako pushnúť zmeny

  cd ~/dami-prototype
  git add .
  git commit -m "popis zmeny"
  git push

  # Ak treba nastaviť token znova:
  git remote set-url origin https://leumasdam:TVOJ_TOKEN@github.com/leumasdam/dami-prototype.git

  GitHub Personal Access Token: github.com/settings/tokens
  (potrebuje scope: repo)

---

## GitHub Pages

  URL:    https://leumasdam.github.io/dami-prototype/
  Branch: main
  Path:   /
  Aktualizuje sa automaticky po každom git push (cca 1-2 min)

---

## Ďalšie kroky (TODO)

  [ ] Responzívny dizajn (mobile breakpoints)
  [ ] Skutočné produktové fotky namiesto emoji
  [ ] Product detail stránka
  [ ] Košík ako slide-out panel
  [ ] Vyhľadávanie produktov
  [ ] Filtrovanie podľa ceny (range slider)
  [ ] Animácia pri scroll na každej sekcii (already: trust bar + general reveal)
  [ ] Prepojenie s reálnym backendom / Shopify

---

## Kontext projektu

Toto je UX/UI redesign prototyp vytvorený s Claude Code (Anthropic).
Pôvodný web: https://www.dami-pracovne-odevy.sk
Vlastník: Adriána Piknová – DAMI, Piešťany
Kontakt: damiobchod@gmail.com / 0902 482 244

Prototyp nie je napojený na skutočný e-shop.
Slúži ako vizuálna a UX demonštrácia.
