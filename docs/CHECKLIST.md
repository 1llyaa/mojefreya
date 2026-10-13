# MojeFreya – zadání část 1 + feedback #2: checklist

Zdroj: „MojeFreya – zadání pro programátora (část 1)“, 11. 10. 2026, a feedback #2.

Vlastník: **T** = šablona (kód, Claude) · **A** = klikání v Shopify adminu · **I** = potřebný vstup / rozhodnutí · **X** = explorace → odpověď a návrh pro Lukáše

Stav: `[ ]` čeká · `[~]` rozpracováno / čeká na vstup · `[x]` hotovo a ověřeno

> Pozor: živé téma `mojefreya/main` je napojené na GitHub. Push do `main` = okamžitě živě.

## 1. Šablona (T) – první část

### Texty a tvrzení
- [x] **A5** H1 „Dlouhodobě hladká pokožka bez holení“
- [x] **A6** „po 2–4 ošetřeních“; „aplikace“ → „ošetření“ v celé šabloně
- [x] **A7** Podnadpis „Domácí IPL epilátor. Šetrně k pokožce.“; karta „Šetrné a bezpečné“
- [x] **D8** Nadpis „Proč Freya PRO“
- [x] **D7** FAQ 15 otázek (FAQ 11 = 300 000 záblesků, pracovní hodnota – ověřit), první dvě rozbalené; „žiletka“ → „holicí strojek“ v O produktu
- [x] **C4** Garance „Vyzkoušejte 60 dní doma“ + text
- [x] **B7** Horní lišta „Doprava 69 Kč · 60 dní na vrácení“; fold „Zásilkovna 69 Kč · doručení do 3 pracovních dnů“; garance jen 60 dní
- [x] **B8** „Platba kartou, Apple Pay, Google Pay nebo na dobírku (+40 Kč)“

### Cena
- [x] **A4** Přeškrtnutá 3 999 Kč + 1 999 Kč: fold, spodní lišta, /products/ipl, /collections/all, /cart
- [x] **F2-1** Formát „1 999 Kč“ s nezlomitelnou mezerou (snippet `price`)
- [x] **B1** Tlačítko „Koupit za 1 999 Kč“, spodní lišta „Koupit“, skok do pokladny zůstává
- [x] **B11** Cena ve foldu 28 px

### Fold
- [x] **B3** Popis produktu ve foldu skrytý (zůstává v produktu)
- [x] **B9** Řádek „FREYA PRO · IPL EPILÁTOR“ nad H1 (13 px, verzálky, 0.08em, #5F564F)
- [x] **B2** Spodní lišta až po odscrollování hlavního tlačítka (mobil i desktop)
- [x] **B6** (volitelné, tečky zůstávají přes fotku) Tečky galerie 24×24, #807C78, mobil slide 88 %, desktop náhledy 64×64

### Globální styly
- [x] **F2-2** Burgundy #A62B4D jen na hlavním tlačítku a tlačítku ve spodní liště
- [x] **F2-3** H2 28 px mobil / 36 px desktop
- [~] **W2** Nadpisy 600 – přepínač Nastavení šablony › Typografie › Písmo nadpisů (Instrument Serif 400 / Source Serif 4 600 / Instrument Sans 600); výchozí beze změny. Čeká: Lukáš vybere, pak zbytek odstranit

### Patička a důvěra
- [~] **A1** Provozovatel: Delina Czechia s.r.o., IČO 11792094, Vítkova 188/22, 186 00 Praha 8 (z ARES), tel. 737 199 066 ✓ · čeká: e-mail podpory → Nastavení šablony › Obchodní údaje › E-mail podpory
- [x] **A8** Odkazy v patičce česky, klikací výška min. 44 px
- [x] **A9** Platební ikony Visa, Mastercard, Apple Pay, Google Pay + „Dobírka“
- [x] **C5** Blok „Kdo jsme“ nad patičkou
- [x] **D9** Blok s cenou a „Koupit za 1 999 Kč“ pod FAQ
- [~] **C6** Ikony wallet, stopwatch, feather, sparkles, return (I: freya-grafika.zip)
- [~] **E1** Favicon 32×32 a 180×180 (I: freya-grafika.zip)

### Recenze (po schválení X4)
- [ ] **C3** Řádek „84 % · 22 ověřených recenzí na Heurece“ pod H1, skok na recenze, bez dat skrytý
- [ ] **C2** Sekce recenzí pod foldem: průměr, počet, 3 recenze s datem, odkaz na Heureku

### Texty zásad (T připraví, A vloží)
- [x] **A2** Návrhy v `docs/policies/` (doplnit e-mail, DIČ, spisovou značku; doporučena kontrola právníkem) → vložit v adminu
- [x] **A3** `docs/policies/02-vraceni-a-reklamace.md`

## 2. Admin (A)

- [ ] **F2-1** Nastavení › Obchod › Formát měny: `{{amount_no_decimals_with_space_separator}} Kč`
- [ ] **A4** Varianta: cena 1 999, porovnávací cena 3 999
- [ ] **A7** Popis produktu: „zpomalují opětovný růst chloupků“, „bezbolestné“ → „šetrné“
- [ ] **A2/A3** Vložit texty do Nastavení › Zásady
- [ ] **A8** Menu `footer-1`: odebrat z patičky nebo přejmenovat odkazy česky
- [ ] **E1** Online Store › Preferences: title, meta description, obrázek pro sdílení 1200×630
- [ ] **K1** Odebrat PayPal a Klarnu
- [ ] **K2** Expresní pokladna jen Apple Pay a Google Pay (vypnout Shop Pay, PayPal)
- [ ] **K3** „Platební karta“, jen Visa a Mastercard
- [ ] **K4** Kontakt: povinný e-mail; doručovací adresa: povinný telefon
- [ ] **K5** Ověřit, že po K2 zmizel „Zapamatovat si mě“
- [ ] **K6** Dobírka pojmenovaná „Na dobírku“
- [ ] **K7** Dobírka bez rozporu (podle X1)
- [ ] **K8** Názvy doprav „Výdejní místo nebo box (Zásilkovna, AlzaBox)“ (+ „, dobírka“) a popis o výběru místa
- [ ] **X3** Odhad doručení u obou doprav „do 3 pracovních dnů“
- [ ] **A4b/A4c** Heureka feed: prodejní cena 1 999 Kč, doručení do 3 pracovních dnů
- [ ] **W1** Nastavení › Ochrana soukromí zákazníků podle rozhodnutí W1
- [ ] **X5** Testovací objednávka: výběr výdejního místa, i u dobírky

## 3. Vstupy (I)

- [ ] freya-grafika.zip (ikony, favicony, og:image)
- [ ] E-mail podpory (fallback na e-mail účtu obchodu záměrně vypnutý – je to soukromý gmail)
- [ ] Potvrdit IČO 11792094 a sídlo Vítkova 188/22, Praha 8 (ARES); DIČ / plátce DPH?
- [ ] Tarif Shopify a seznam aplikací (feed, Zásilkovna, cookies, měření)
- [ ] Export recenzí z Heureky / API klíč
- [ ] Lukáš: počet záblesků (FAQ 11), ověřit FAQ 1, 6, 7, 8
- [ ] Lukáš: rozhodnutí W1, W2, X1

## 4. Explorace (X) – výstup pro Lukáše

- [ ] **X1** Dobírka: varianta a/b/c, ident-system.cz, aplikace a tarif
- [~] **X2** Checkbox Heureky v košíku – vkládá ho app block aplikace „Heureka Zboží Tracking“ (`templates/cart.json`, přidáno v editoru), ne šablona
- [ ] **X3** Doba doručení a expedice do dalšího pracovního dne
- [ ] **X4** Recenze z Heureky: widget vs. import
- [ ] **X5** Výběr výdejního místa
- [ ] **W1** Které měřicí skripty web načítá
- [ ] **W2** Náhrada písma pro nadpisy 600
- [ ] **A4b** Odkud bere Heureka feed cenu
- [ ] **K3** Které značky karet jdou vypnout, kde se mění název

## 5. Poznámky k nasazení

- Změny jsou jen lokálně (necommitnuté). Živé téma `mojefreya/main` se nasadí pushem do `main` na GitHubu.
- `templates/index.json`, `templates/product.json`, `sections/footer-group.json` jsou soubory editoru – před pushem znovu `git pull`, ať se nepřepíšou změny z editoru.
- Ve footer-group je menu `footer-1` odpojené; zásady se vypisují samy s českými názvy.
- `shopify theme dev` hlásí produkt jako nedostupný (tlačítko „Vyprodáno“), živý web ho má dostupný – jde o prostředí náhledu, ne o šablonu.
