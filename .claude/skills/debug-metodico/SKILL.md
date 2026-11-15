---
name: debug-metodico
description: Trova la causa di un errore con un metodo a ipotesi e prove, invece di cambiare codice a tentativi. Usala quando l'utente dice "non funziona", "dà errore", "si è rotto", "perché fa così", incolla un messaggio di errore o descrive un comportamento strano.
---

# Debug metodico

Regola d'oro: **non correggere niente finché non sai perché succede.** Una correzione senza causa
spesso nasconde il problema e ne crea un altro.

## Procedura

1. **Descrivi il sintomo con precisione.** Cosa ci si aspettava, cosa succede invece, da quando,
   se succede sempre o a volte. Raccogli il messaggio di errore completo.
2. **Riproduci.** Trova i passi minimi che fanno comparire il problema. Se non si riproduce, prima
   raccogli più dati (log, versioni, ambiente): senza riproduzione non c'è verifica.
3. **Cosa è cambiato?** Ultime modifiche al codice, aggiornamenti di librerie, dati nuovi, ambiente diverso.
   `git log` e `git diff` sono spesso la via più corta.
4. **Formula 2–3 ipotesi** e per ognuna scrivi quale osservazione la confermerebbe o la smentirebbe.
5. **Fai l'esperimento più economico** che separa le ipotesi: un `console.log`/`print`, un test
   piccolo, dimezzare l'input, commentare metà del codice (ricerca binaria).
6. **Leggi il risultato onestamente.** Se smentisce la tua ipotesi preferita, cambiala.
7. **Correggi la causa**, con la modifica più piccola possibile.
8. **Dimostra la correzione:** il caso che falliva ora passa, e aggiungi un test che fallirebbe se il
   bug tornasse.
9. **Pulisci** i log temporanei.

## Domande utili quando si è bloccati
- Il codice che sto guardando è davvero quello che viene eseguito? (cache, build vecchia, file sbagliato)
- I dati sono quelli che penso? Stampali invece di supporli.
- L'errore nasce qui o arriva da prima?

## Errori da evitare
- Cambiare tre cose insieme: se funziona non sai quale ha risolto.
- Disattivare un test che fallisce per "far tornare verde".
- Dichiarare risolto senza aver rieseguito il caso che falliva.
