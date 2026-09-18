# Discovery: Il topo ladro

## Obiettivo

Realizzare un gioco browser breve e comico in cui il giocatore aiuta un topo a rubare tre alimenti in una casa, evitando il gatto e usando un mobiletto come nascondiglio.

## Stakeholder

| Stakeholder | Interesse | Responsabilità |
| --- | --- | --- |
| Giocatore | Divertimento e obiettivo chiaro | Muovere il topo e scegliere quando rischiare |
| Team studenti | Apprendere Spec Driven Development | Progettare, sviluppare e testare il gioco |
| Docente | Valutare il processo | Verificare documenti e collaborazione |
| Tester | Esperienza stabile | Verificare regole, controlli e casi limite |

## Scope MVP

### Incluso

- Una stanza vista dall'alto.
- Un topo controllabile.
- Tre cibi da raccogliere.
- Un gatto con pattuglia semplice e inseguimento breve.
- Due mobiletti in cui nascondersi.
- Una tana da raggiungere.
- Vittoria, sconfitta e riavvio.

### Escluso

- Multiplayer, inventario complesso, salvataggi, economia, livelli procedurali e backend.

## Requisiti funzionali

- [RF-001] Il giocatore deve poter muovere il topo nella stanza.
- [RF-002] Il giocatore deve poter raccogliere i tre cibi richiesti.
- [RF-003] Il gatto deve pattugliare e inseguire il topo quando lo vede.
- [RF-004] Il giocatore deve potersi nascondere nei mobiletti.
- [RF-005] La vittoria deve avvenire raggiungendo la tana con tutti i cibi.
- [RF-006] La sconfitta deve avvenire quando il gatto raggiunge il topo fuori dal nascondiglio.

## Requisiti non funzionali

- [RNF-001] Il gioco deve funzionare senza dipendenze o server applicativo.
- [RNF-002] I controlli devono essere spiegati nella schermata iniziale.
- [RNF-003] Stati, obiettivi e pericoli devono essere distinguibili anche con testo e icone.
- [RNF-004] Una partita deve durare circa 2-4 minuti.

## Rischi e assunzioni

| ID | Tipo | Descrizione | Mitigazione |
| --- | --- | --- | --- |
| R-001 | Rischio | Il gatto potrebbe sembrare casuale | Pattuglia e inseguimento con avviso visivo |
| R-002 | Rischio | Il giocatore potrebbe non capire cosa manca | Contatore cibi sempre visibile |
| A-001 | Assunzione | Una sola stanza è sufficiente per l'MVP | Rimandare livelli multipli |
| A-002 | Assunzione | Il mouse può essere controllato con tastiera | Aggiungere touch solo in una fase successiva |

## Domande aperte

- Il punteggio verrà aggiunto dopo il primo playtest?
- Il gatto deve emettere un suono o è sufficiente il feedback visivo?
