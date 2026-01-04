# SitoPerTesi

Questo progetto contiene un sito statico (pagine HTML) e una libreria di contenuti audio associati ai capitoli (letture e musiche), più i jingle per ciascun capitolo.

## Struttura del progetto

La root di lavoro è `src/`:

- `src/website/html/`  
  Contiene le pagine HTML del sito:
    - `index.html` (home)
    - `capitolo1.html` … `capitolo6.html` (pagine dei capitoli)
    - `privacy.html` (privacy)

- `src/audio/`  
  Contiene tutti i contenuti audio e i testi associati:
    - `Capitolo 1/` … `Capitolo 6/`
        - `Lettura testo/`  
          Contiene file di testo (`.txt`) e relative registrazioni (`.wav`) per i paragrafi/parti del capitolo.
          Esempio:
            - `src/audio/Capitolo 2/Lettura testo/Paragrafo 2.1.txt`
            - `src/audio/Capitolo 2/Lettura testo/Paragrafo 2.1.wav`
        - `Musiche/` (presente dove necessario)  
          Contiene brani/estratti in formato `.mp3` collegati al capitolo.
    - `Jingles/`  
      Contiene i jingle di sottofondo di lettura per capitolo in `.mp3`, uno per ciascun capitolo.

## Come funziona il sito

- Il sito è **statico**: le pagine sono file HTML in `src/website/html/`.
- I contenuti multimediali (letture/musiche/jingle) sono in `src/audio/`.
- Ogni capitolo ha normalmente:
    - una pagina dedicata (`capitoloN.html`);
    - una cartella `src/audio/Capitolo N/` con:
        - `Lettura testo/` (testi e letture)
        - `Musiche/` (eventuali brani)
    - un jingle in `src/audio/Jingles/` con il nome che include `Capitolo N`.

## Convenzioni di naming (contenuti)

- **Letture**: coppie `.txt` + `.wav` con lo stesso nome base (es. `Paragrafo 3.2.txt` e `Paragrafo 3.2.wav`).
- **Musiche**: file `.mp3` con titolo descrittivo.
- **Jingles**: un `.mp3` per capitolo, con `Capitolo N` nel nome.

## Mappa rapida dei percorsi

- Home: `src/website/html/index.html`
- Capitoli: `src/website/html/capitolo1.html` … `src/website/html/capitolo6.html`
- Privacy: `src/website/html/privacy.html`
- Audio capitoli: `src/audio/Capitolo X/`
- Jingle: `src/audio/Jingles/`