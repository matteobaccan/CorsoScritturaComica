# Corso di Scrittura Comica

[![Genera PDF](https://github.com/matteobaccan/CorsoScritturaComica/actions/workflows/generatepdf.yml/badge.svg)](https://github.com/matteobaccan/CorsoScritturaComica/actions/workflows/generatepdf.yml)

Corso di introduzione alla scrittura comica tenuto da Federico Basso.

## Appunti del corso di Federico Basso del 8 Maggio 2010

Anni fa ho avuto il piacere di partecipare ad un corso di scrittura comica tenuto da Federico Basso, comico e autore di Zelig.

Il corso era a Torino, nella sede della [Quinta Tinta](https://www.facebook.com/QuintaTintaImprovvisazione/?locale=it_IT) e mi ha permesso di sperimentare un approccio diverso alla scrittura.

Spero che queste slide possano aiutare anche altri a scoprire questo mondo.

__[Scarica gratuitamente le slide](https://raw.githubusercontent.com/matteobaccan/CorsoScritturaComica/main/slide/Corso_ScritturaComica.pdf)__

## Cosa insegna il corso

L'idea di fondo è che **troppa libertà = nessuna libertà**: le battute non nascono dall'ispirazione libera, ma da vincoli e tecniche precise. Le slide raccolgono, con esempi ed esercizi fatti in aula:

- **Le tre regole base**: immedesimarsi in un personaggio, avere un obiettivo certo, scrivere in prima persona al presente.
- **La seconda battuta**: la prima idea che viene in mente è la più scontata; la creatività inizia dalla seconda.
- **Premessa e chiusa**: la premessa deve spiazzare l'ascoltatore, la chiusa (la parola che fa ridere) va in fondo alla frase.
- **La regola del 3**: in una lista, vero → verosimile → assurdo. I primi due elementi creano il pattern, il terzo lo rompe (la lista della spesa di Marilyn Manson).
- **Spiazzamento** (reverse misdirection): la premessa fa immaginare una direzione, la chiusa va altrove.
- **Lavorare per immagini**: la chiusa deve evocare un'immagine concreta, non un concetto astratto.
- **Pensiero laterale**: in una situazione solenne, una reazione banale e quotidiana ("prima frase sul suolo lunare: ma ho preso le chiavi della navicella?").
- **Giochi di parole**: storpiature di nomi e titoli famosi, sostituzioni di lettere, proverbi rivisitati.
- **Il monologo**: come collegare le battute tra loro partendo da un argomento vasto e da una mappa mentale (oggetti, concetti astratti, persone, problemi).

## Skill per Claude Code

Il repository include una skill ([`.claude/skills/scrittura-comica`](.claude/skills/scrittura-comica/SKILL.md)) che trasforma gli appunti del corso in un metodo operativo per [Claude Code](https://claude.com/claude-code): non un riassunto delle slide, ma una "recipe" che l'AI segue passo per passo quando scrive materiale comico.

### Come si usa

Apri questo repository con Claude Code e:

- invoca la skill direttamente con `/scrittura-comica`, oppure
- chiedi semplicemente di scrivere battute, freddure, liste comiche o un monologo su un tema: la skill viene attivata automaticamente quando il compito è di scrittura comica.

Esempi di richieste:

```text
/scrittura-comica
Scrivi 5 battute sul traffico in città
Fai un monologo comico sugli smartphone
Rendi più divertente questo testo: ...
```

### Come funziona

Per ogni battuta la skill impone il metodo del corso:

1. **Immedesimazione**: sceglie chi parla e in quale situazione concreta.
2. **Genera almeno 3 idee e scarta la prima**, che è quella che direbbe chiunque (su smartphone: Siri, batteria scarica...).
3. **Costruisce premessa e chiusa**: premessa che spiazza o esagera, parola comica in fondo alla frase.
4. **Sceglie una tecnica** adatta al contesto: regola del 3, spiazzamento, lavoro per immagini, pensiero laterale, storpiature, battuta a incastro.
5. **Verifica una checklist finale**: chiusa come ultima immagine della frase, prima persona al presente, niente chiuse "talmente tanto che" (struttura da esercizio, vietata nelle battute finite), niente barzellette ("c'era un tizio...").

Per i monologhi la skill segue la struttura insegnata al corso: argomento vasto → mappa mentale su quattro assi (oggetti, astratto, persone, problemi) → una battuta per nodo → battute concatenate con transizioni, iniziando dalle più facili.

La skill è stata sviluppata con un approccio "test-driven": le battute generate senza skill mostravano esattamente i difetti che il corso insegna a evitare (prime idee scontate, chiuse astratte, pattern "così... che"); con la skill attiva questi difetti spariscono.

## Licenza

Il contenuto di questo repository è distribuito con licenza [GPL-3.0](LICENSE).
