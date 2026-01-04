# Configurazione GitHub Pages

Questo documento spiega come configurare GitHub Pages per pubblicare il sito.

## Passaggi per la configurazione

1. **Vai nelle Impostazioni del Repository**
   - Accedi al repository su GitHub
   - Clicca su "Settings" (Impostazioni)

2. **Configura GitHub Pages**
   - Nel menu laterale sinistro, clicca su "Pages"
   - Nella sezione "Source" (Sorgente), seleziona:
     - **Branch**: `main` (o il branch principale del tuo repository)
     - **Folder**: `/docs`
   - Clicca su "Save" (Salva)

3. **Attendi la pubblicazione**
   - GitHub Pages richiede alcuni minuti per elaborare e pubblicare il sito
   - Vedrai un messaggio che indica l'URL del sito pubblicato
   - L'URL sarà del tipo: `https://d4mi4n0.github.io/LaStoriaDellaComputerMusic/`

## Verifica

Dopo la pubblicazione, il sito sarà accessibile all'indirizzo mostrato nelle impostazioni di GitHub Pages.

Puoi verificare che tutto funzioni correttamente:
- La homepage dovrebbe essere visibile all'URL principale
- Tutti i capitoli dovrebbero essere accessibili cliccando sui link
- I file audio dovrebbero essere riproducibili nelle pagine dei capitoli

## Struttura dei file

Il sito è pubblicato dalla cartella `/docs`:
- `/docs/index.html` → Homepage
- `/docs/capitolo1.html` - `/docs/capitolo6.html` → Pagine dei capitoli
- `/docs/privacy.html` → Privacy policy
- `/docs/audio/` → Tutti i file audio (letture, musiche, jingle)
- `/docs/.nojekyll` → File che impedisce a GitHub Pages di processare il sito con Jekyll

## Aggiornamenti

Per aggiornare il sito:
1. Modifica i file sorgente in `src/`
2. Copia i file aggiornati nella cartella `/docs`
3. Assicurati che i percorsi audio rimangano corretti (`audio/`)
4. Commit e push delle modifiche
5. GitHub Pages aggiornerà automaticamente il sito pubblicato (può richiedere alcuni minuti)

## Note importanti

- Il file `.nojekyll` nella cartella `/docs` è necessario per evitare che GitHub Pages processi i file con Jekyll
- I percorsi audio nei file HTML sono relativi alla cartella `/docs` e puntano a `audio/`
- Tutti i link tra le pagine sono relativi (es. `capitolo2.html`, `index.html`)
