# Miry's book — guida al sito

Il sito è fatto di pochi file. Questi due sono i soli che contengono i tuoi contenuti,
e **non devi mai aprirli a mano**: li compili dal pannello.

| File | Cosa contiene |
|---|---|
| `prodotti.json` | L'elenco dei prodotti |
| `impostazioni.json` | Nome, numero WhatsApp, email, orari, P. IVA |
| `index.html` | La grafica del sito (si tocca solo per cambi di aspetto) |
| `.pages.yml` | La configurazione del pannello |
| `immagini/` | Le foto dei prodotti |

---

## 1. Account GitHub

1. Vai su **github.com** → *Sign up*.
2. Mail, password, nome utente. Il nome utente finirà nell'indirizzo del sito, quindi scegline uno pulito (es. `mirysbook`).
3. Conferma la mail.
4. Attiva l'autenticazione a due fattori quando te la propone: questo account è la chiave di tutto.

## 2. Il repository

1. In alto a destra **+** → *New repository*.
2. **Repository name**: `mirys.book`
3. Spunta **Public**. Non aggiungere README, .gitignore o licenza.
4. *Create repository*.

## 3. Caricare i file

Nella pagina del repository vuoto: **uploading an existing file**.

Trascina **tutti** questi elementi insieme:

- `index.html`
- `prodotti.json`
- `impostazioni.json`
- `.pages.yml`
- `.nojekyll`
- la cartella `immagini`

In fondo alla pagina premi **Commit changes**.

> Se `.pages.yml` o `.nojekyll` non si lasciano trascinare perché il computer li
> considera file nascosti: *Add file* → *Create new file*, scrivi il nome del file
> nella casella in alto, incolla il contenuto, *Commit changes*.

## 4. Mettere il sito online

1. Nel repository: **Settings** (in alto) → **Pages** (menù a sinistra).
2. Sotto *Build and deployment* → *Source*: **Deploy from a branch**.
3. *Branch*: **main**, cartella **/ (root)** → **Save**.
4. Aspetta un paio di minuti e ricarica: in cima compare l'indirizzo del sito.

L'indirizzo sarà `https://TUONOME.github.io/mirys.book/`. È pubblico: lo metti in bio su Instagram, lo mandi su WhatsApp, lo stampi su un biglietto.

## 5. Il pannello (Pages CMS)

1. Vai su **pagescms.org** → *Sign in* → entra con GitHub.
2. GitHub ti chiede di autorizzare Pages CMS: scegli **Only select repositories** e seleziona `mirys.book`.
3. Torni sul pannello e vedi il repository. Cliccalo.
4. A sinistra trovi **Prodotti** e **Impostazioni del sito**.

### Aggiungere un prodotto

*Prodotti* → **Add an entry** → compili i campi → **Save**.

- **Categoria** è un menù: scegli, non scrivere.
- **Foto**: carichi dal computer o dal telefono. Se la lasci vuota resta il disegno scelto in *Disegno*.
- **Etichetta rossa**: lascia vuoto se non serve.
- **In vetrina**: spegnilo per nascondere un prodotto esaurito senza perderlo.

Dopo *Save*, il sito si aggiorna da solo in uno o due minuti. Se non vedi la modifica, ricarica la pagina con `Ctrl+F5`.

### Cambiare numero, email, nome

*Impostazioni del sito*. Occhio ai due campi del telefono:

- **Numero WhatsApp per i link**: solo cifre, prefisso senza `+` → `393331234567`
- **Numero come si legge sul sito**: come preferisci → `+39 333 123 4567`

Il primo fa funzionare i pulsanti, il secondo è solo quello che legge il cliente.

## 6. Prima di dirlo in giro

- [ ] Numero WhatsApp vero in *Impostazioni*
- [ ] Email vera
- [ ] P. IVA (se non ce l'hai ancora, svuota il campo: la riga sparisce)
- [ ] Prova da telefono: apri il sito, premi *Chiedi il prezzo*, controlla che WhatsApp si apra sulla tua chat
- [ ] Cancella i prodotti che non fai e aggiungi i tuoi

## 7. Il dominio tuo (facoltativo)

Compri `mirysbook.it` da un registrar (Aruba, Namecheap, Cloudflare), poi in
*Settings → Pages → Custom domain* scrivi il dominio e segui le istruzioni DNS.
Il sito resta gratis, paghi solo il dominio (circa 15–20 € l'anno).

---

## Se qualcosa non va

**Il pannello dice che manca la configurazione** → `.pages.yml` non è stato caricato, o è finito dentro una sottocartella invece che nella radice del repository.

**Il sito è online ma il catalogo dice "Catalogo non raggiungibile"** → manca `prodotti.json` nella radice, oppure il file è stato modificato a mano e ha un errore di virgole.

**Le foto non si vedono** → controlla che nel campo foto ci sia un percorso tipo `immagini/nomefoto.jpg` e non un indirizzo che inizia con `http`.

**Ho rotto qualcosa** → GitHub tiene la storia di ogni salvataggio: scheda *Commits*, apri quello di prima, *Revert*. Niente è perso davvero.
