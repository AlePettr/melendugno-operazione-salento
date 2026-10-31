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
