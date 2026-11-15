# Modelli di prompt

Da copiare in qualsiasi chat con Claude. I segnaposto sono tra `{graffe}`.

---

## 1. Riassunto per chi deve decidere
**Serve a:** ridurre un documento lungo a ciò che serve per prendere una decisione.

```
<documento>
{testo}
</documento>

Devo decidere {decisione}. Dal documento estrai:
1. la risposta breve (2 frasi) a cosa conviene fare e perché;
2. i 3 fatti che la sostengono, con la frase del documento da cui li prendi;
3. cosa manca nel documento per decidere con sicurezza.
Se il documento non contiene un'informazione, scrivi "non indicato" invece di supporre.
```

---

## 2. Email o messaggio delicato
**Serve a:** scrivere un messaggio difficile (reclamo, rifiuto, sollecito) con il tono giusto.

```
Devo scrivere a {destinatario e rapporto con me} per {scopo}.
Situazione: {fatti, in breve}.
Tono: {cordiale ma fermo / formale / amichevole}.
Il messaggio deve ottenere: {azione concreta che voglio dal destinatario}.
Massimo {N} righe. Dammi due versioni: una più diretta e una più morbida.
```

---

## 3. Chiedere codice
**Serve a:** ottenere codice che funziona nel tuo contesto, non un esempio generico.

```
Linguaggio/ambiente: {es. JavaScript con Node 22, nessuna libreria esterna}
Cosa deve fare: {comportamento, con un esempio di input e output atteso}
Dove va: {file o funzione esistente}
<codice_esistente>
{codice}
</codice_esistente>
Vincoli: {prestazioni, compatibilità, stile del progetto}
Dopo il codice, scrivi un test che dimostri il caso d'esempio.
```

---

## 4. Analizzare un errore
**Serve a:** far trovare la causa invece di una correzione a caso.

```
Mi aspetto: {comportamento atteso}
Succede invece: {comportamento reale}
Messaggio di errore completo:
<errore>
{errore}
</errore>
Ultima cosa cambiata prima del problema: {modifica}
Prima di proporre correzioni, elenca le possibili cause in ordine di probabilità e dimmi
quale controllo fare per distinguerle.
```

---

## 5. Imparare un argomento
**Serve a:** studiare qualcosa di nuovo partendo dal proprio livello.

```
Voglio capire {argomento}. Conosco già {cosa so}. Mi serve per {scopo pratico}.
Spiegamelo in 5 passi, dal più semplice al più avanzato. Dopo ogni passo fammi una domanda
di verifica e aspetta la mia risposta prima di continuare.
```

---

## 6. Far criticare il proprio lavoro
**Serve a:** ricevere critiche utili invece di complimenti.

```
<lavoro>
{testo, piano o codice}
</lavoro>
Comportati da revisore esigente. Trova i 3 punti più deboli, in ordine di gravità, e per
ognuno spiega cosa potrebbe andare storto in pratica e come rimediare. Niente complimenti.
```
