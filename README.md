# Melendugno: Operazione Salento — v0.3

Sparatutto 3D nel browser ambientato nelle vie di Melendugno (LE). Strade ed edifici vengono dai dati OpenStreetMap e sono ricostruiti in 3D in prima persona.

## Avvio
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

## Novità v0.3
- Ricostruzione completa: niente più mappa 2D sotto, ora è un vero mondo 3D
- Edifici estrusi dalle impronte OSM con finestre e tetti, strade, collisioni precise con scorrimento sui muri
- Prima persona con arma, terza persona opzionale, minimappa, audio sintetizzato
- Droni con IA semplice, linea di tiro con occlusione dagli edifici, danno e game over / vittoria

## Limiti
Edifici low-poly senza facciate reali; altezze stimate dai livelli OSM (o 2–3 piani se mancano). Niente pathfinding, veicoli, salvataggi o multiplayer. I droni sono bersagli fittizi.

Dati mappa © OpenStreetMap contributors (ODbL). Rispettare attribuzione e policy dei servizi.
