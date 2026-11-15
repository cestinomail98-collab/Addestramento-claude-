---
name: progetto-da-zero
description: Porta un'idea a una prima versione funzionante e testata, in passi piccoli e verificabili. Usala quando l'utente dice "voglio creare un'app", "fammi un programma che…", "costruiamo un sito per…", "da dove comincio", o descrive un gestionale, uno strumento o un gioco da realizzare.
---

# Da un'idea a una prima versione

## Procedura

1. **Capire il lavoro vero.** Chi lo userà, su che dispositivo, cosa fa oggi senza lo strumento.
   Chiedi 2–3 esempi concreti di uso ("arriva un camion con 4 container: cosa si registra?").
2. **Scrivere le regole in chiaro.** Elenca le regole del dominio in frasi semplici e falle confermare
   all'utente prima di scrivere codice. Sono la parte che più spesso si sbaglia.
3. **Scegliere il minimo.** Quali 3–5 funzioni rendono lo strumento utile già domani? Il resto va in
   una lista "dopo".
4. **Scegliere la tecnologia più semplice che basta.** Meno dipendenze = meno cose che si rompono.
   Dichiara subito cosa è prototipo e cosa sarà reale (dati condivisi, accessi, backup).
5. **Separare le regole dall'interfaccia.** Le regole del dominio in un modulo unico, usato da tutto il
   resto. Così si testano senza interfaccia e non si duplicano.
6. **Test sulle regole** con i casi d'esempio del punto 1, prima o insieme al codice.
7. **Interfaccia minima**, poi provala davvero (avvia l'app, fai le operazioni, guarda il risultato).
8. **Dati dimostrativi** generati passando dalle stesse operazioni reali, non scritti a mano:
   così sono sempre coerenti con le regole.
9. **Consegna con istruzioni**: come si avvia, cosa fa, cosa manca, cosa serve per andare in produzione.

## Errori da evitare
- Costruire tutto prima di far provare qualcosa all'utente.
- Presentare un prototipo come se fosse sicuro o pronto per dati veri.
- Inventare regole del dominio invece di chiederle.
