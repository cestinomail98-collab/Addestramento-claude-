# Caso: revisione-codice

**Skill provata:** `revisione-codice`

## Prompt da inviare

````
Rivedi questa funzione prima che la metta in produzione:

```js
app.post('/scarico', async (req, res) => {
  const { lotto, tonnellate } = req.body;
  const giacenza = await db.get(`SELECT qta FROM lotti WHERE codice = '${lotto}'`);
  if (giacenza.qta > tonnellate) {
    await db.run(`UPDATE lotti SET qta = qta - ${tonnellate} WHERE codice = '${lotto}'`);
  }
  res.json({ ok: true });
});
```
````

## Cosa ci si aspetta da una risposta buona
In ordine di gravità, con scenario concreto per ciascuno:
1. **SQL injection**: `lotto` e `tonnellate` finiscono direttamente nella query.
2. **Nessun controllo di accesso**: chiunque può scaricare merce.
3. **Due scarichi contemporanei** leggono la stessa giacenza e la portano sotto zero
   (serve una transazione o un `UPDATE … WHERE qta >= ?`).
4. `giacenza` è `undefined` se il lotto non esiste → errore non gestito.
5. `>` invece di `>=`: non si può scaricare esattamente tutta la giacenza.
6. Risponde `ok: true` anche quando lo scarico non è avvenuto.
7. `tonnellate` non è validato (negativo, testo, zero).

## Segnali di risposta scadente
- Mette al primo posto lo stile (nomi, `async`, formattazione).
- Trova l'injection ma non la concorrenza o la risposta falsa `ok: true`.

## Risultati
_(da compilare con la scheda di valutazione)_
