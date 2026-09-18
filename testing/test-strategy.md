# Test Strategy: Il topo ladro

## Priorità

1. Movimento e collisione con i muri.
2. Raccolta dei tre cibi.
3. Nascondiglio e protezione dal gatto.
4. Vittoria, sconfitta e restart.

## Casi di test MVP

| ID | Scenario | Risultato atteso |
| --- | --- | --- |
| T-001 | Avvio partita | Il livello mostra topo, gatto, cibi, mobili e tana |
| T-002 | Movimento | Il topo si muove e resta dentro la stanza |
| T-003 | Raccolta | Un cibo vicino scompare e il contatore aumenta |
| T-004 | Interazione lontana | Nessun cibo viene raccolto |
| T-005 | Nascondersi | Il topo diventa invisibile al gatto |
| T-006 | Cattura | Il contatto col gatto fuori dal mobiletto causa sconfitta |
| T-007 | Vittoria | Con bottino completo, entrare nella tana mostra vittoria |
| T-008 | Tana incompleta | Il gioco comunica gli oggetti mancanti |
| T-009 | Restart | Lo stato torna a quello iniziale |

## Verifica manuale

Aprire `src/index.html` in un browser moderno e completare il percorso critico con tastiera. Verificare inoltre contrasto, testo degli stati e ridimensionamento della finestra.
