# Addestramento-claude-

Serie di prompt, skill e test per ampliare le capacità di Claude, condivisi tra chi lavora con Claude.

## Come funziona davvero (leggere prima)

Questa repository **non modifica il modello**: Claude non impara dai file che mettiamo qui e non
ricorda le conversazioni tra una sessione e l'altra. Quello che fa è dare a Claude **contesto pronto
all'uso**, ogni volta che lo apri su questa cartella:

| Cosa | Dove | Quando viene usato |
|---|---|---|
| **Istruzioni di progetto** | `CLAUDE.md` | Claude Code lo legge automaticamente all'avvio |
| **Skill** | `.claude/skills/<nome>/SKILL.md` | Claude Code le carica quando il compito corrisponde alla descrizione, oppure con `/<nome>` |
| **Modelli di prompt** | `prompt/` | Da copiare e incollare in qualsiasi chat con Claude |
| **Test** | `test/` | Per verificare se un prompt o una skill migliora davvero le risposte |
| **Sapienze** | `sapienze/` | Lezioni pratiche raccolte lavorando con Claude |

Per usare le skill in un altro progetto basta copiare la cartella della skill dentro
`.claude/skills/` di quel progetto (o in `~/.claude/skills/` per averle ovunque).

## Skill disponibili

| Skill | A cosa serve |
|---|---|
| [`scrivere-prompt`](.claude/skills/scrivere-prompt/SKILL.md) | Trasformare una richiesta vaga in un prompt chiaro e verificabile |
| [`revisione-codice`](.claude/skills/revisione-codice/SKILL.md) | Revisione del codice orientata ai bug reali, non allo stile |
| [`debug-metodico`](.claude/skills/debug-metodico/SKILL.md) | Trovare la causa di un errore con ipotesi e prove, senza tentativi a caso |
| [`progetto-da-zero`](.claude/skills/progetto-da-zero/SKILL.md) | Da un'idea a una prima versione funzionante e testata |
| [`spiegare-semplice`](.claude/skills/spiegare-semplice/SKILL.md) | Spiegare un argomento tecnico a chi non è del mestiere |
| [`crea-skill`](.claude/skills/crea-skill/SKILL.md) | Scrivere una nuova skill per questa raccolta |

## Struttura

```
CLAUDE.md                 regole comuni per Claude in questa repository
CONTRIBUTING.md           come aggiungere skill, prompt e test
.claude/skills/           le skill (una cartella ciascuna, con SKILL.md)
prompt/                   modelli di prompt riutilizzabili
test/                     scheda di valutazione e casi di prova
sapienze/                 lezioni pratiche
```

## Collaborare

Leggi [CONTRIBUTING.md](CONTRIBUTING.md). In breve: un ramo per ogni contributo, una pull request,
e per ogni skill nuova almeno un caso in `test/casi/` che mostri cosa migliora.
