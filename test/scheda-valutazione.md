# Scheda di valutazione

Serve a capire se una skill o un prompt migliora davvero le risposte, invece di affidarsi
all'impressione.

## Come si fa un test
1. Prendi il caso da `test/casi/`.
2. Apri **due sessioni nuove** di Claude: una con la skill (o il prompt migliorato), una senza.
3. Invia lo stesso testo in entrambe.
4. Dai i voti qui sotto a entrambe le risposte **senza guardare quale è quale**, se possibile
   (fatele copiare in un file da un'altra persona, mescolate).
5. Ripeti almeno 3 volte: le risposte variano, un solo tentativo non basta.
6. Annota i risultati in fondo al file del caso.

## Criteri (da 0 a 2)

| Criterio | 0 | 1 | 2 |
|---|---|---|---|
| **Corretto** | Contiene errori | Corretto ma incompleto | Corretto e completo |
| **Segue le istruzioni** | Ignora vincoli | Ne rispetta una parte | Li rispetta tutti |
| **Utile** | Non si può usare | Serve qualche ritocco | Si usa così com'è |
| **Onesto** | Inventa o esagera | Qualche affermazione non sostenuta | Dice cosa non sa |
| **Chiaro** | Confuso o prolisso | Comprensibile | Diretto e ordinato |

Totale massimo: 10. Una skill vale la pena se migliora il totale medio in modo stabile.

## Modulo risultati

```
Data: {gg/mm/aaaa}   Chi ha provato: {iniziali}   Modello: {nome mostrato nell'app}
Tentativo | Senza skill | Con skill | Note
1         |  /10        |  /10      |
2         |  /10        |  /10      |
3         |  /10        |  /10      |
```
