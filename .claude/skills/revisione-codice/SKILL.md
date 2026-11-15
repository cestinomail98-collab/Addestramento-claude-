---
name: revisione-codice
description: Revisione del codice che cerca bug reali e rischi concreti invece di commenti sullo stile. Usala quando l'utente chiede "rivedi questo codice", "controlla le modifiche", "ci sono bug?", "fai una code review", o prima di unire una pull request.
---

# Revisione del codice

Lo scopo è trovare ciò che **si rompe**, non ciò che si potrebbe scrivere diversamente.

## Procedura

1. **Capisci l'intento.** Leggi la descrizione della modifica o chiedila. Una riga di codice è giusta o
   sbagliata solo rispetto a cosa doveva fare.
2. **Leggi tutta la modifica**, poi il codice intorno che la chiama o ne dipende.
3. **Cerca in quest'ordine:**
   1. Correttezza: logica sbagliata, casi limite (vuoto, zero, negativo, `null`, liste di un elemento,
      date a cavallo di mezzanotte o cambio d'ora), condizioni invertite, errori di uno (`<` contro `<=`).
   2. Dati: cosa succede con input malformato, duplicato, molto grande, in arrivo due volte.
   3. Concorrenza: due utenti o due richieste nello stesso momento.
   4. Sicurezza: input dell'utente usato in query, comandi, HTML o percorsi file; permessi controllati
      sul server e non solo nell'interfaccia; segreti scritti nel codice o nei log.
   5. Errori: eccezioni ignorate, messaggi che non aiutano, stato lasciato a metà.
   6. Test: la modifica è coperta? I test verificano davvero il comportamento o solo che "non esplode"?
4. **Verifica ogni sospetto** prima di riportarlo: costruisci lo scenario concreto
   ("con l'input X, la riga Y restituisce Z invece di W"). Se non riesci a costruirlo, scartalo o
   segnalalo come dubbio, non come bug.
5. **Riporta** in ordine di gravità.

## Formato del resoconto

```
1. [GRAVE] file.js:42 — Descrizione in una frase.
   Scenario: con {input}, succede {risultato sbagliato} invece di {atteso}.
   Correzione proposta: {in breve}.
```

Se non trovi problemi reali, dillo chiaramente. Un resoconto vuoto è un risultato valido.

## Errori da evitare
- Riempire il resoconto di preferenze di stile: annegano i problemi veri.
- Segnalare bug "possibili" senza scenario.
- Riscrivere tutto il codice invece di indicare la correzione minima.
