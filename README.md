# Relazione Sito web di una pizzeria

**Progetto:** `pizzeria_anaclerio_pisani_squeo`  
**Classe:** 5Bi  
**Gruppo:** Anaclerio Mattia, Pisani Christian, Squeo Flavio  
**Repository:** <https://github.com/mattiCleri0/pizzeria_anaclerio_pisani_squeo>

---

## 1. Scopo dell'esercitazione

Simulare la collaborazione tra diversi sviluppatori per l'implementazione del sito (con relativo menù) di una pizzeria.

Obiettivi:

1. collaborare come sviluppatori distinti sullo stesso progetto, usando Git e GitHub;
2. realizzare la pagina menù della pizzeria;
3. realizzare la pagina contatti;
4. realizzare la pagina prenotazioni;
5. realizzare la pagina index (home page).

---

## 2. Organizzazione del gruppo

Ciascuno ha lavorato su un branch dedicato, e il codice è stato poi integrato nel branch main tramite Pull Request.

### Flusso di lavoro Git

1. Creazione del repository con il commit iniziale.
2. Creazione di un branch per ciascuna funzionalità.
3. Sviluppo in autonomia della propria pagina.
4. Apertura di una Pull Request verso main e relativa unione (merge).
5. Integrazione finale del file README.md sul branch main.

---

## 3. Struttura del progetto

```
pizzeria_anaclerio_pisani_squeo/
├── index.html            # Home page
├── menu.html             # Menù (antipasti e pizze)
├── contatti.html         # Contatti, form messaggi, mappa
├── prenotazione.html     # Form di prenotazione tavolo
├── visualizza.html       # Archivio delle prenotazioni
├── styles.css            # Stile della home page
├── style_m.css           # Stile del menù
├── styles_pren_vis.css   # Stile di prenotazione e archivio
├── img/
│   ├── antipasti.jpg
│   ├── tagliere.jpg
│   ├── margherita.jpg
│   ├── diavola.jpg
│   ├── quattro_formaggi.jpg
│   └── immagini.md
└── README.md
```

---

## 4. Descrizione delle pagine

### 4.1 Home page – index.html
Pagina di benvenuto della pizzeria. Contiene l'intestazione con slogan, una sezione di presentazione, quattro pulsanti di navigazione (Menu, Le Nostre Pizze, Prenota un Tavolo, Contatti) e un piè di pagina con indirizzo, telefono e P.IVA. Con gli stili definiti in stile è definito in styles.css.

### 4.2 Menù – menu.html
Presenta il menù suddiviso in due sezioni, ciascuna con "card" contenenti foto, nome, prezzo e descrizione:

| Categoria | Piatto | Prezzo |
|---|---|---|
| Antipasti | Fritturina Mista | € 6,00 |
| Antipasti | Tagliere di Formaggi | € 8,00 |
| Pizze | Margherita | € 6,50 |
| Pizze | Diavola | € 8,00 |
| Pizze | Quattro Formaggi | € 8,50 |

In fondo è presente un pulsante per tornare alla home.

### 4.3 Contatti – contatti.html
Contiene indirizzo, telefono, e-mail, orari di apertura e profili social, un form per inviare un messaggio (con validazione dei campi obbligatori e un messaggio di conferma tramite JavaScript) e una mappa Google Maps incorporata. Il CSS è scritto direttamente nella pagina.

### 4.4 Prenotazione – prenotazione.html
Form suddiviso in tre sezioni: dati del cliente, per quando prenotare e dove sedersi. Funzionalità principali:

- scelta del "turno" (pranzo o cena) con l'elenco degli orari disponibili;
- data minima impostata automaticamente al giorno corrente;
- numero di persone da 1 a 20;
- scelta della sala (interna, vicino al forno a legna, esterna) e campo note.

### 4.5 Archivio prenotazioni – visualizza.html
Riceve i dati del form tramite parametri URL, li salva nel localStorage del browser e li mostra in una tabella. Permette di eliminare una singola prenotazione o di svuotare l'intero archivio (con richiesta di conferma). Il contenuto viene inserito con textContent, evitando l'iniezione di HTML, e l'URL viene ripulito dopo l'invio per non duplicare la prenotazione con un aggiornamento della pagina.

---

## 5. Tecnologie utilizzate

- HTML5 per la struttura delle pagine
- CSS3
- JavaScript (manipolazione del DOM, localStorage, URLSearchParams)
- Git e GitHub (branch, commit, Pull Request, merge)
- Markdown per la documentazione

---

## 6. Conclusioni

L'esercitazione ha permesso al gruppo di mettere in pratica una modalità di lavoro collaborativa: ripartizione dei compiti, sviluppo su branch separati e integrazione tramite Pull Request. Gli obiettivi richiesti (home page, menù e contatti) sono stati raggiunti, e il sito è stato arricchito con un sistema di prenotazione funzionante.

Sono state riscontrate delle incongruenze nei file, nella fase di sviluppo, mostrando l'importanza di definire in anticipo alcune regole comuni (nomi, dati, struttura dei file, stile, ecc...) e di dedicare un momento finale alla revisione incrociata del codice, aspetto fondamentale nello sviluppo software in team.
