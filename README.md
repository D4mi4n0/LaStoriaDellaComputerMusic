# SitoPerTesi

Questo progetto contiene un sito statico (pagine HTML) e una libreria di contenuti audio associati ai capitoli (letture e musiche), più i jingle per ciascun capitolo.

## Struttura del progetto

Il sito è pubblicato tramite GitHub Pages dalla cartella `/docs`.

### Struttura di pubblicazione (GitHub Pages)

- `/docs/`  
  Contiene i file pubblicati su GitHub Pages:
    - `index.html` (home)
    - `capitolo1.html` … `capitolo6.html` (pagine dei capitoli)
    - `privacy.html` (privacy)
    - `.nojekyll` (impedisce a Jekyll di processare i file)
    - `audio/` - Contiene tutti i contenuti audio e i testi associati

- `/docs/audio/`  
  Contiene tutti i contenuti audio e i testi associati:
    - `Capitolo 1/` … `Capitolo 6/`
        - `Lettura testo/`  
          Contiene file di testo (`.txt`) e relative registrazioni (`.wav`) per i paragrafi/parti del capitolo.
          Esempio:
            - `docs/audio/Capitolo 2/Lettura testo/Paragrafo 2.1.txt`
            - `docs/audio/Capitolo 2/Lettura testo/Paragrafo 2.1.wav`
        - `Musiche/` (presente dove necessario)  
          Contiene brani/estratti in formato `.mp3` collegati al capitolo.
    - `Jingles/`  
      Contiene i jingle di sottofondo di lettura per capitolo in `.mp3`, uno per ciascun capitolo.

### Struttura sorgente

- `src/website/html/`  
  Contiene i file HTML sorgente (da copiare in `/docs` per la pubblicazione)

- `src/audio/`  
  Contiene i file audio sorgente (da copiare in `/docs/audio` per la pubblicazione)

## Come funziona il sito

- Il sito è **statico**: le pagine sono file HTML pubblicati nella cartella `/docs`.
- I contenuti multimediali (letture/musiche/jingle) sono in `/docs/audio/`.
- Ogni capitolo ha normalmente:
    - una pagina dedicata (`capitoloN.html`);
    - una cartella `docs/audio/Capitolo N/` con:
        - `Lettura testo/` (testi e letture)
        - `Musiche/` (eventuali brani)
    - un jingle in `docs/audio/Jingles/` con il nome che include `Capitolo N`.

## Pubblicazione su GitHub Pages

Il sito è configurato per essere pubblicato tramite GitHub Pages dalla cartella `/docs`. 

Per aggiornare il sito pubblicato:
1. Modificare i file sorgente in `src/`
2. Copiare i file modificati nella cartella `/docs`
3. Assicurarsi che i percorsi audio puntino a `audio/` (relativo alla cartella docs)
4. Commit e push delle modifiche

GitHub Pages servirà automaticamente il contenuto dalla cartella `/docs` all'indirizzo configurato nelle impostazioni del repository.

## Convenzioni di naming (contenuti)

- **Letture**: coppie `.txt` + `.wav` con lo stesso nome base (es. `Paragrafo 3.2.txt` e `Paragrafo 3.2.wav`).
- **Musiche**: file `.mp3` con titolo descrittivo.
- **Jingles**: un `.mp3` per capitolo, con `Capitolo N` nel nome.

## Mappa rapida dei percorsi

### Pubblicazione (GitHub Pages)
- Home: `/docs/index.html`
- Capitoli: `/docs/capitolo1.html` … `/docs/capitolo6.html`
- Privacy: `/docs/privacy.html`
- Audio capitoli: `/docs/audio/Capitolo X/`
- Jingle: `/docs/audio/Jingles/`

### Sorgenti
- Home: `src/website/html/index.html`
- Capitoli: `src/website/html/capitolo1.html` … `src/website/html/capitolo6.html`
- Privacy: `src/website/html/privacy.html`
- Audio capitoli: `src/audio/Capitolo X/`
- Jingle: `src/audio/Jingles/`