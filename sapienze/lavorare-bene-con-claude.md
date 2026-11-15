# Lavorare bene con Claude

Lezioni pratiche. Aggiungine di vostre in fondo, con un esempio reale.

## Cosa Claude è e non è
- **Non ricorda** le conversazioni precedenti, a meno che l'app non abbia una memoria attiva o tu non
  gli ridia il contesto. Per questo servono file come `CLAUDE.md` e le skill.
- **Non impara** da questa repository: legge i file quando lavora qui, come un collega che consulta un
  manuale. Migliorare i file migliora le risposte; il modello resta lo stesso.
- **Può sbagliare con sicurezza.** Su fatti, date, prezzi e versioni di programmi chiedi la fonte o fai
  verificare. Su codice chiedi i test e falli eseguire.

## Cosa fa la differenza
1. **Dare il perché.** "Scrivi breve" funziona meno di "scrivi breve perché si legge dal telefono in
   magazzino". Con il motivo, Claude prende decisioni giuste anche nei casi non previsti.
2. **Esempi concreti.** Un caso reale ("arrivano 3 container in 2 giorni…") chiarisce più di una
   descrizione astratta.
3. **Chiedere prima di costruire.** Per lavori grandi, chiedi prima un piano o le regole in elenco e
   correggile: costa un minuto e risparmia ore.
4. **Verificare, non fidarsi.** "Funziona?" → "fammi vedere il test che passa" o "avvialo e mostrami il
   risultato".
5. **Un compito per volta** quando i compiti sono diversi. Si possono concatenare dopo.
6. **Correggere con precisione.** "Non va bene" non aiuta; "il totale deve escludere i lotti già
   spediti" sì.

## Lezioni da un progetto reale (gestionale di magazzino)
- **Una sola fonte per le regole.** Le regole del magazzino stavano in un unico modulo usato sia
  dall'interfaccia sia dal server: niente doppioni che divergono, e test facili.
- **Dati di prova generati dalle operazioni vere.** Invece di scrivere i dati demo a mano, si fanno
  passare carichi e scarichi reali dal motore: i dati sono sempre coerenti.
- **Dichiarare cosa è demo e cosa è reale.** Una versione dimostrativa senza password va bene, purché
  sia scritto chiaramente a schermo e nella documentazione cosa serve per usarla con dati veri
  (server, accessi, HTTPS, backup).
- **Test sui casi che fanno paura**: due persone che scaricano lo stesso lotto nello stesso istante, la
  stessa richiesta inviata due volte, permessi di chi non dovrebbe poter fare qualcosa.

## Sicurezza minima
- Non incollare in chat password, chiavi API o dati personali di altri.
- Prima di eseguire un comando che Claude propone e che cancella o modifica molte cose, chiedi cosa
  fa esattamente.
