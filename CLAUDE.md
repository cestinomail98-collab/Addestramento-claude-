# Istruzioni per Claude in questa repository

Questa repository raccoglie skill, prompt e test condivisi da più persone. Quando ci lavori:

## Lingua e tono
- Scrivi in italiano, in modo diretto. Frasi brevi, niente giri di parole.
- Usa i termini tecnici quando servono, ma spiegali la prima volta se il lettore potrebbe non conoscerli.

## Modo di lavorare
- Prima di creare un file nuovo, controlla se ne esiste già uno simile da ampliare.
- Una skill fa **una cosa sola**. Se una skill cresce troppo, dividila.
- Ogni affermazione su cosa "migliora" Claude va sostenuta da un caso in `test/casi/`.
  Niente promesse non verificate.
- Non scrivere mai che una skill o un prompt "addestra" il modello: danno contesto, non cambiano i pesi.

## Formato delle skill
- Percorso: `.claude/skills/<nome-in-minuscolo-con-trattini>/SKILL.md`
- Intestazione YAML con `name` (uguale alla cartella) e `description`.
- La `description` dice **quando** usarla, con le frasi che un utente scriverebbe davvero.
- Corpo: procedura in passi numerati, poi errori da evitare. Sotto le 150 righe se possibile.

## Sicurezza
- Mai inserire password, token, chiavi API, email o dati personali nei file.
- Gli esempi usano dati inventati e dichiarati come tali.

## Prima di chiudere un lavoro
- Aggiorna la tabella delle skill nel `README.md` se ne hai aggiunta o rinominata una.
- Verifica che i collegamenti relativi nei file Markdown puntino a file esistenti.
