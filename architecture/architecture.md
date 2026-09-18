# Architecture: Il topo ladro

## Decisione

Per l'MVP si usa una pagina statica con HTML, CSS e JavaScript. Lo stato della partita è in memoria; non serve persistenza.

## Componenti

| Componente | Responsabilità | Non responsabilità |
| --- | --- | --- |
| Game state | Possiede fase, posizione, bottino e stato NPC | Rendering diretto |
| Game loop | Aggiorna movimento, collisioni e tempo | Testo della UI |
| Input controller | Traduce tastiera in comandi | Regole di vittoria |
| World entities | Rappresenta topo, gatto, cibi, tana e mobili | Layout della pagina |
| Renderer/UI | Mostra mondo, obiettivo e feedback | Decisioni di gioco |

## Pattern architetturali

- State machine per `ready`, `playing`, `won` e `lost`.
- Entity model leggero per le entità del livello.
- Separazione input-update-render nel loop principale.

## Dipendenze

```text
Input -> Game State <- Game Loop -> Entities
                         |
                         v
                      Renderer/UI
```

## Flusso principale

```text
Input del giocatore
       |
       v
Aggiornamento stato -> Collisioni -> Regole vittoria/sconfitta -> Rendering
```

## Persistenza

Non necessaria per l'MVP. Eventuali punteggi possono essere aggiunti in seguito con localStorage senza introdurre un backend.

## Motivazioni

La soluzione riduce setup e dipendenze, rende il gioco apribile subito in un browser e permette al team di concentrare il workshop su specifica, collaborazione e test.
