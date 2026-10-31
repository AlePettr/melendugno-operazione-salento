# Melendugno: Operazione Salento

Sparatutto 3D nel browser ambientato nelle vie di Melendugno (LE). Strade ed edifici vengono dai dati OpenStreetMap e sono ricostruiti in 3D in prima persona.

## Modalità
- `index.html` — menu iniziale
- `streetview.html` — **Street View + HUD**: foto reali di Google, spostamento a salti lungo la strada, droni sovrapposti con proiezione 3D, radar, checkpoint. Richiede una chiave API Google Maps (Maps JavaScript API) inserita nella schermata iniziale e salvata solo nel browser. Limita la chiave ai referrer del sito (`https://alepettr.github.io/*`). Mantieni visibili logo e note legali di Google.
- `osm.html` — paese 3D da OpenStreetMap (v0.3, vedi sotto), gratis e senza chiavi

### Street View: note
- Muoversi: W/S o frecce su/giù (passi lungo i link di Street View), A/D o frecce sinistra/destra per girare, trascina col mouse per guardarti attorno, click o Spazio per sparare
- Niente collisioni né occlusione: i droni volano sopra la strada e si vedono sempre
- Se i droni sembrano disallineati rispetto all'immagine, regola la costante `FOVK` in `streetview.html`

## Avvio (paese 3D)
Apri la pagina GitHub Pages della repo, oppure in locale: `python -m http.server 8000` e visita `http://localhost:8000`.
Serve connessione internet (Three.js da CDN e dati OpenStreetMap via Overpass API). Al primo avvio i dati vengono salvati nel browser (cache locale).
Se Overpass non risponde, il gioco usa un paese di prova generato, così resta giocabile.

## Controlli
- WASD / frecce: movimento · Shift: corsa
- Mouse: mira (il primo clic blocca il puntatore) · Click / Spazio: sparo
- R: ricarica · V: visuale prima/terza persona · Esc: pausa
- Touch: metà sinistra = movimento, metà destra = visuale, pulsante FUOCO

## Missione
1. Raggiungi il punto di controllo (fascio di luce arancione, freccia e distanza nell'HUD, minimappa).
2. Neutralizza i 5 droni ostili: ti inseguono e sparano, e non vedono attraverso gli edifici.

## Aggiornamento grafica
- Strade asfaltate con marciapiede, alberi lungo le vie, palette più contrastata, nebbia più lontana
- Partenza e obiettivo scelti nelle zone più dense di edifici

## Novità v0.3
- Ricostruzione completa: niente più mappa 2D sotto, ora è un vero mondo 3D
- Edifici estrusi dalle impronte OSM con finestre e tetti, strade, collisioni precise con scorrimento sui muri
- Prima persona con arma, terza persona opzionale, minimappa, audio sintetizzato
- Droni con IA semplice, linea di tiro con occlusione dagli edifici, danno e game over / vittoria

## Limiti
Edifici low-poly senza facciate reali; altezze stimate dai livelli OSM (o 2–3 piani se mancano). Niente pathfinding, veicoli, salvataggi o multiplayer. I droni sono bersagli fittizi.

Dati mappa © OpenStreetMap contributors (ODbL). Rispettare attribuzione e policy dei servizi.
