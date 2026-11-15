---
name: crea-skill
description: Guida alla scrittura di una nuova skill per Claude Code in questa raccolta, con test per verificarla. Usala quando l'utente dice "creiamo una skill", "voglio insegnare a Claude a…", "aggiungi una skill per…", o vuole trasformare un procedimento ripetuto in istruzioni riutilizzabili.
---

# Creare una nuova skill

Una skill è un file di istruzioni che Claude carica quando il compito lo richiede. Serve quando un
procedimento si ripete e Claude, senza indicazioni, lo farebbe in modo diverso da come lo vogliamo.

## Procedura

1. **Raccogli un caso reale.** Chiedi all'utente un esempio di richiesta e di risultato ideale.
   Meglio ancora: uno in cui Claude senza skill ha sbagliato o fatto diversamente.
2. **Scegli il nome:** minuscolo, con trattini, verbo o compito (`preventivo-cliente`, `verbale-riunione`).
3. **Scrivi la descrizione** (è la parte più importante: decide quando la skill si attiva):
   - cosa fa, in una frase;
   - "Usala quando…" con le frasi che l'utente scriverebbe davvero.
4. **Scrivi il corpo:**
   - titolo e una riga sullo scopo;
   - `## Procedura` in passi numerati, ognuno verificabile;
   - eventuale schema o esempio di risultato;
   - `## Errori da evitare`, presi da sbagli realmente visti.
   Spiega il *perché* delle regole importanti: Claude generalizza meglio da un motivo che da un ordine.
5. **File di supporto** (modelli, script, esempi lunghi) vanno nella stessa cartella e si citano dal
   `SKILL.md`, così non appesantiscono il file principale.
6. **Scrivi il test** in `test/casi/<nome>.md` usando `test/scheda-valutazione.md`.
7. **Prova con e senza la skill** lo stesso prompt e confronta. Se non c'è differenza, la skill non serve
   o la descrizione non la attiva.
8. **Aggiorna il `README.md`.**

## Modello

```markdown
---
name: nome-skill
description: Fa X. Usala quando l'utente dice "…", "…", o quando …
---

# Titolo

Scopo in una riga.

## Procedura
1. …
2. …

## Errori da evitare
- …
```

## Errori da evitare
- Descrizioni generiche ("aiuta con i documenti"): la skill si attiva a caso o mai.
- Skill enciclopediche: se supera ~150 righe, dividila o sposta il materiale in file di supporto.
- Regole senza motivo, scritte in maiuscolo.
