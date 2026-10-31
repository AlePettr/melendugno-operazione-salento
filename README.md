# Melendugno: Operazione Salento — v0.2

## Avvio
Apri `index.html` con connessione internet. Se il browser limita l'accesso locale, avvia un server:
`python -m http.server 8000` e visita `http://localhost:8000`.

## Controlli
- WASD / frecce: movimento
- Mouse: ruota la visuale (clic sul canvas per bloccare il puntatore)
- Click / Spazio: sparo
- R: ricarica
- Shift: corsa
- Pulsante FUOCO e trascinamento sul lato destro: controlli touch

## Correzioni v0.2.1
- La missione ora avanza: il checkpoint si attiva entro 12 m (prima la soglia era in metri ma scritta come gradi, quindi irraggiungibile)
- Velocità di movimento corretta (prima ~200 m/s)
- W/S e A/D ora seguono la direzione in cui guarda il personaggio
- Edifici OSM posizionati e animati rispetto al giocatore, con collisioni corrette
- Mouse: clic per bloccare il puntatore, poi clic per sparare
- Avviso a schermo se Leaflet/Three.js non si caricano

## Novità v0.2
- Edifici con impronte OpenStreetMap estruse in 3D tramite Overpass API, se il servizio è disponibile
- Collisioni circolari semplificate con gli edifici caricati
- Animazione procedurale degli arti
- Droni che si muovono
- Missione in due fasi con checkpoint
- Camera di inseguimento in terza persona

## Limiti
È ancora un prototipo: la mappa cartografica resta 2D; gli edifici 3D sono una prima estrusione semplificata, non modelli architettonici accurati. Le collisioni sono approssimate. Non sono ancora presenti animazioni scheletriche, pathfinding, veicoli, audio, salvataggi o multiplayer. I droni sono bersagli fittizi.
Dati mappa © OpenStreetMap contributors; dati edificio richiesti a Overpass API. Rispettare attribuzione e policy dei servizi.
