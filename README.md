# Giobicom25 - Portfolio Progetti 2025

Repository principale per i progetti e sviluppi del 2025. Un portfolio moderno e funzionale che raccoglie tutti i progetti realizzati durante l'anno.

## 🚀 Caratteristiche

- **Design Moderno**: Interfaccia pulita con Bootstrap 5 Dark Theme
- **Font Monospace**: Utilizzo del font JetBrains Mono per un look professionale da developer
- **Responsive**: Completamente ottimizzato per tutti i dispositivi
- **Animazioni**: Transizioni fluide e hover effects eleganti

## 📁 Struttura del Progetto

```
giobicom25/
├── index.html              # Homepage principale del portfolio
├── README.md               # Documentazione del progetto
└── project/                # Cartella contenente tutti i progetti
    └── stresasalute.it/    # Progetto Stresa Salute
        ├── index.html      # Homepage del progetto
        └── img/            # Immagini del progetto
            └── cover.jpg   # Immagine di copertina del progetto
```

## 🎨 Design e Tecnologie

### Homepage (index.html)
- **Bootstrap 5**: Framework CSS con tema dark
- **JetBrains Mono**: Font monospace per un look professionale
- **Hero Section**: Sezione di benvenuto con immagine AI generata
- **Portfolio Projects**: Sezione dedicata ai progetti con cards animate
- **Responsive Design**: Ottimizzato per desktop, tablet e mobile

### Immagini
- **Copertina Principale**: Immagine AI generata tramite URL personalizzabile
- **Copertine Progetti**: Immagini statiche nella cartella `./img` di ogni progetto
- **Fallback**: Placeholder automatici in caso di immagini mancanti

## 📊 Progetti Inclusi

### 1. Stresa Salute (`project/stresasalute.it/`)
- **Descrizione**: Piattaforma web dedicata alla salute e al benessere nella zona di Stresa
- **Tipo**: Applicazione web per servizi sanitari locali
- **Anno**: 2025
- **Immagine**: `./project/stresasalute.it/img/cover.jpg`

## 🛠️ Installazione e Uso

1. **Clone del repository**:
   ```bash
   git clone https://github.com/tuousername/giobicom25.git
   cd giobicom25
   ```

2. **Apertura locale**:
   - Apri `index.html` direttamente nel browser
   - Oppure usa un server locale per un'esperienza ottimale

3. **Aggiunta di nuovi progetti**:
   - Crea una cartella in `project/nome-progetto/`
   - Aggiungi l'`index.html` del progetto
   - Crea la cartella `img/` con l'immagine `cover.jpg`
   - Aggiorna la sezione progetti nell'`index.html` principale

## 🎯 Personalizzazione

### Modifica dell'immagine di copertina principale
Sostituisci l'URL nell'`index.html`:
```html
<img src="TUA_URL_IMMAGINE_AI" alt="Immagine di copertina AI generata">
```

### Aggiunta di nuovi progetti
1. Crea la struttura cartelle del progetto
2. Aggiungi una nuova card nella sezione progetti dell'`index.html`
3. Assicurati di includere l'immagine di copertina in `./project/nome-progetto/img/cover.jpg`

## 🌟 Funzionalità Speciali

- **Smooth Scrolling**: Navigazione fluida tra le sezioni
- **Hover Effects**: Animazioni al passaggio del mouse
- **Error Handling**: Gestione automatica delle immagini mancanti
- **SEO Friendly**: Struttura ottimizzata per i motori di ricerca
- **Accessibility**: Design accessibile e inclusivo

## 📱 Compatibilità

- ✅ Chrome/Chromium
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile browsers

## 🚧 Roadmap

- [ ] Aggiunta sistema di filtri per progetti
- [ ] Integrazione con API GitHub per stats automatiche
- [ ] Dark/Light theme toggle
- [ ] Sezione blog/articoli
- [ ] Sistema di contatti integrato

## 📄 Licenza

Questo progetto è rilasciato sotto licenza MIT. Vedi il file `LICENSE` per maggiori dettagli.

---

**Ultimo aggiornamento**: 18 Giugno 2025
**Versione**: 1.0.0
