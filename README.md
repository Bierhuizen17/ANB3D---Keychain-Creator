# ANB3D Keychain Creator

Webtool van **ANB3D – 3D Print Service** om 3D-sleutelhangers, naamplaatjes en labels uit tekst te maken en te downloaden als **STL** voor 3D-printen.

## Functies
- Tekst (meerdere regels) in 15 lettertypes, optioneel vetgedrukt
- Twee stijlen: blokjes of glad reliëf
- Plaatvormen: afgeronde rechthoek, rechthoek, ovaal, cirkel, zeshoek, ster, hart, label met punt, of geen plaat
- Plaatgrootte van 70% tot 220%
- Ophangoog als ring in de vorm van de plaat, of alleen een gat (boven of links)
- Randafwerking: afgeschuind, afgerond, opstaande rand, dubbele rand
- Kleuren, hoogte, detailniveau en breedte in mm instelbaar
- STL-export in millimeters, plat en klaar voor je slicer

## Gebruiken
Alles zit in één bestand: `index.html`. Geen build of installatie nodig.

Lokaal: open `index.html` in je browser, of start een server:

```
python3 -m http.server 8000
```

en ga naar http://localhost:8000.

## Online zetten met GitHub Pages
1. Maak een nieuwe repository op GitHub en upload alle bestanden uit deze map (of gebruik `git push`).
2. Ga naar **Settings → Pages**.
3. Kies bij **Source** voor **GitHub Actions**. De meegeleverde workflow in `.github/workflows/pages.yml` zet de site dan automatisch online bij elke push naar `main`.
   - Liever zonder Actions? Kies **Deploy from a branch**, branch `main`, map `/ (root)`.
4. Na een minuut staat de tool op `https://<gebruikersnaam>.github.io/<repositorynaam>/`.
5. Eigen domein? Voeg dat toe onder **Settings → Pages → Custom domain**.

## Technische notities
- Three.js (r128) wordt geladen via cdnjs en de lettertypes via Google Fonts, dus de pagina heeft internet nodig. Wil je volledig offline werken, download dan `three.min.js` en de lettertypes en verwijs ernaar vanuit `index.html`.
- Het logo zit als afbeelding in `index.html` ingebed.
- Tip: controleer een STL altijd in je slicer vóór je print, vooral bij ster, hart en dubbele rand.

## Licentie
Nog niet gekozen. Voeg zelf een `LICENSE` toe als je de code wilt delen, en vergeet niet dat het logo en de merknaam ANB3D van jou blijven.
