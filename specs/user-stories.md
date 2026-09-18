# User Stories: Il topo ladro

## US-001: Muovere il topo

Come giocatore, voglio muovere il topo nella stanza, così posso esplorare e pianificare il furto.

### Acceptance criteria

- Given una partita attiva, when premo una freccia o `WASD`, then il topo si muove nella direzione scelta.
- Il topo non può attraversare i muri.

## US-002: Rubare il cibo

Come giocatore, voglio raccogliere i cibi richiesti, così posso completare il furto.

### Acceptance criteria

- Vicino a un cibo, `E` o `Spazio` lo aggiunge al bottino.
- Il contatore mostra quanti cibi sono stati raccolti.
- Ogni cibo raccolto scompare dalla stanza.

## US-003: Evitare il gatto

Come giocatore, voglio capire quando il gatto mi vede, così posso reagire prima di perdere.

### Acceptance criteria

- Il gatto segue una pattuglia visibile.
- Quando vede il topo, mostra uno stato di allerta e lo insegue.
- Se raggiunge il topo fuori da un nascondiglio, la partita termina.

## US-004: Nascondersi

Come giocatore, voglio nascondermi in un mobiletto, così posso evitare il gatto.

### Acceptance criteria

- Vicino a un mobiletto, `E` o `Spazio` nasconde il topo.
- Il gatto non può catturare il topo nascosto.
- Premendo nuovamente il comando, il topo esce dal mobiletto.

## US-005: Tornare alla tana

Come giocatore, voglio raggiungere la tana con tutto il cibo, così posso vincere.

### Acceptance criteria

- La tana diventa completabile solo dopo aver raccolto tutti i cibi.
- Entrando nella tana con il bottino completo, compare la schermata di vittoria.
- È possibile ricominciare la partita dopo vittoria o sconfitta.
