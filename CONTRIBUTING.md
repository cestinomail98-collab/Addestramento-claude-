# Come contribuire

## Flusso
1. Crea un ramo: `git checkout -b nome/argomento` (es. `marco/skill-excel`).
2. Aggiungi o modifica i file.
3. Apri una pull request e chiedi una revisione all'altro.
4. Si unisce quando entrambi siete d'accordo.

## Aggiungere una skill
1. Crea `.claude/skills/<nome>/SKILL.md` partendo da una skill esistente (o usa `/crea-skill`).
2. Scrivi almeno un caso di prova in `test/casi/` con il prompt, cosa ci si aspetta e come si giudica.
3. Prova il caso **con e senza** la skill e annota il risultato nella pull request.
4. Aggiungi la skill alla tabella del `README.md`.

## Aggiungere un prompt
Mettilo in `prompt/modelli.md` sotto la sezione giusta, con:
- a cosa serve (una riga),
- il testo del prompt con i segnaposto tra `{graffe}`,
- un esempio compilato.

## Aggiungere una sapienza
Una lezione va in `sapienze/` se è nata da un caso reale. Scrivi: cosa è successo, cosa si è
imparato, come applicarlo la prossima volta. Niente dati personali o aziendali riservati.

## Regole comuni
- Italiano chiaro, frasi brevi.
- Nessuna credenziale, email o dato personale nei file.
- Se modifichi la skill di un altro, spiega il motivo nella pull request.
