# Game Design: Il topo ladro

## Core Gameplay Loop

1. Osserva il percorso del gatto.
2. Muovi il topo verso un alimento.
3. Raccogli il cibo.
4. Nasconditi se il gatto si avvicina.
5. Ripeti fino a completare il bottino.
6. Raggiungi la tana e vinci.

## Obiettivi

- Obiettivo principale: raccogliere tutti i cibi e tornare alla tana.
- Obiettivo secondario: non farsi scoprire e completare il furto senza errori.

## Meccaniche

### M-001: Movimento
- Descrizione: il topo cammina nella stanza.
- Input del giocatore: frecce o `WASD`.
- Comportamento: movimento a velocità costante dentro i muri.
- Risultato: il giocatore raggiunge oggetti e zone sicure.
- Condizioni di successo: posizione aggiornata senza uscire dalla stanza.
- Condizioni di fallimento: tentativo di attraversare un muro, senza penalità.

### M-002: Furto
- Descrizione: il topo raccoglie cibo vicino.
- Input del giocatore: `E` o `Spazio`.
- Comportamento: l'oggetto viene rimosso e il bottino aumenta.
- Risultato: il contatore mostra il progresso.
- Condizioni di successo: il topo è abbastanza vicino al cibo.
- Condizioni di fallimento: il comando è premuto troppo lontano.

### M-003: Nascondiglio
- Descrizione: il topo entra o esce da un mobiletto.
- Input del giocatore: `E` o `Spazio` vicino al mobiletto.
- Comportamento: il topo diventa nascosto e il gatto lo ignora.
- Risultato: il giocatore può aspettare che passi il pericolo.
- Condizioni di successo: il topo è nella zona del mobiletto.
- Condizioni di fallimento: nessun mobiletto abbastanza vicino.

### M-004: Gatto
- Descrizione: NPC che pattuglia e insegue.
- Input del giocatore: nessuno.
- Comportamento: segue punti di pattuglia; se il topo è vicino e non nascosto, insegue.
- Risultato: crea pressione senza rendere il gioco imprevedibile.
- Condizioni di successo: il giocatore evita la linea del gatto.
- Condizioni di fallimento: il gatto raggiunge il topo.

## Controlli

| Azione | Tastiera | Alternativa |
| --- | --- | --- |
| Movimento | Frecce / WASD | Nessuna nell'MVP |
| Interagisci | E / Spazio | Nessuna nell'MVP |
| Riavvia | R | Pulsante sul pannello |

## NPC

### Gatto

- Stato normale: pattuglia lentamente.
- Rilevamento: si allerta quando il topo è entro una distanza breve.
- Inseguimento: si muove verso il topo per pochi secondi.
- Perdita del bersaglio: torna alla pattuglia se il topo si nasconde o si allontana.
- Feedback: colore e testo dello stato sempre visibili.

## Livelli

### Livello 1: La cucina

- Layout: cucina rettangolare con muri e tavolo centrale.
- Oggetti richiesti: formaggio, biscotto e mela.
- Nascondigli: mobiletto a sinistra e dispensa a destra.
- Posizione tana: angolo inferiore sinistro.
- Pericoli: un solo gatto.

## Vittoria

Tutti i cibi raccolti e topo dentro la tana.

## Sconfitta

Il gatto raggiunge il topo non nascosto.

## Progressione

MVP: un livello. Estensione possibile: seconda stanza con due gatti, senza introdurla prima del playtest.

## Edge Cases

| Caso | Comportamento atteso |
| --- | --- |
| Interagisci lontano da un oggetto | Nessuna azione |
| Tana raggiunta senza bottino completo | Mostra quanti oggetti mancano |
| Gatto vicino mentre si entra nel mobiletto | Il nascondiglio protegge se l'interazione è completata |
| Riavvio durante la partita | Reset completo della stanza |
