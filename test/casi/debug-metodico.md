# Caso: debug-metodico

**Skill provata:** `debug-metodico`

## Prompt da inviare

````
Questa funzione dovrebbe dirmi quanti giorni mancano a una consegna, ma a volte sbaglia di uno.

```js
function giorniMancanti(consegna) {
  const oggi = new Date();
  return Math.round((new Date(consegna) - oggi) / 86400000);
}
```

Correggila.
````

## Cosa ci si aspetta da una risposta buona
- **Non** cambia subito il codice a caso: individua le possibili cause prima.
- Nomina almeno due cause reali:
  - l'ora corrente di `oggi` (alle 18:00 mancano "mezzo giorno" in meno, e `round` arrotonda);
  - `new Date("2026-03-30")` viene letta in UTC, mentre `new Date()` è in ora locale;
  - il cambio dell'ora legale rende alcuni giorni lunghi 23 o 25 ore.
- Propone una correzione che confronta **date di calendario** (azzerando l'ora o usando date in UTC).
- Fornisce un test con casi precisi (es. sera tardi, giorno del cambio d'ora).

## Segnali di risposta scadente
- Sostituisce `round` con `ceil` o `floor` senza spiegare perché, e senza test.
- Dichiara risolto senza mostrare un caso che prima falliva e ora passa.

## Risultati
_(da compilare con la scheda di valutazione)_
