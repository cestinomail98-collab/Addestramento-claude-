---
name: scrivere-prompt
description: Trasforma una richiesta vaga in un prompt chiaro, completo e verificabile per Claude o un altro modello. Usala quando l'utente dice "scrivimi un prompt", "migliora questo prompt", "come lo chiedo a Claude", "il prompt non funziona", oppure prepara istruzioni per un agente o un sistema automatico.
---

# Scrivere un prompt efficace

Un buon prompt è quello che un collega bravo ma appena arrivato capirebbe al primo colpo.
Claude non vede cosa c'è nella testa di chi scrive: tutto ciò che conta deve stare nel testo.

## Procedura

1. **Obiettivo in una frase.** Cosa deve esistere alla fine? (un testo, un file, una decisione, un codice)
   Se non si riesce a dirlo in una frase, chiedi all'utente prima di scrivere.
2. **Contesto.** Chi è il lettore finale, perché serve, cosa è già stato provato.
   Il *perché* conta: permette a Claude di decidere bene nei casi non previsti.
3. **Materiale.** Incolla i dati, il codice o i documenti dentro tag riconoscibili:
   `<documento>…</documento>`, `<codice>…</codice>`. Metti il materiale lungo **prima** della domanda.
4. **Vincoli.** Lunghezza, formato, lingua, tono, cosa *non* fare. Formula i divieti anche in positivo
   ("scrivi in paragrafi" funziona meglio di "non usare elenchi").
5. **Esempi.** Uno o due esempi di risultato ideale valgono più di dieci aggettivi.
   Se gli esempi sono tutti uguali, Claude li copierà alla lettera: variali.
6. **Formato di uscita.** Indica esattamente la forma: tabella, JSON con certi campi, sezioni con certi titoli.
7. **Criterio di successo.** Come si capisce che la risposta è buona? Scrivilo: aiuta Claude e aiuta chi giudica.
8. **Rileggi da estraneo.** Togli ciò che è ambiguo, contraddittorio o superfluo.

## Schema pronto

```
Obiettivo: {cosa deve esistere alla fine}

Contesto: {per chi è, perché serve, cosa sappiamo già}

<materiale>
{dati, testo o codice}
</materiale>

Vincoli:
- {lunghezza / formato / tono}
- {cosa evitare, detto in positivo}

Esempio di risultato buono:
{esempio}

Risposta buona se: {criterio verificabile}
```

## Errori da evitare
- Scrivere in MAIUSCOLO o con "IMPORTANTISSIMO": i modelli recenti seguono già le istruzioni, l'enfasi
  eccessiva li rende rigidi e fa esagerare.
- Chiedere "fai del tuo meglio" senza dire cosa significa "meglio".
- Dare istruzioni che si contraddicono (es. "breve" ma "includi tutti i dettagli").
- Nascondere la domanda in mezzo al materiale.
- Chiedere più compiti diversi nello stesso prompt quando si possono separare.
