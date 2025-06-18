# Guideline Grafiche - Giobicom25 Design System

## 🎨 **Tema Base e Filosofia**

### Concept Principale
- **Stile**: Developer-oriented, moderno, professionale
- **Ispirazione**: GitHub Dark Theme, VS Code, Terminal aesthetic
- **Target**: Sviluppatori, tech-savvy professionals, portfolio moderno

---

## 🌈 **Palette Colori**

### Colori Primari
```css
--bg-primary: #0d1117;      /* Background principale (GitHub dark) */
--bg-secondary: #161b22;    /* Background secondario (cards, sezioni) */
--bg-tertiary: #21262d;     /* Background elementi interattivi */
--border-primary: #30363d;  /* Bordi principali */
```

### Colori Accento
```css
--accent-blue: #58a6ff;     /* Blu principale (link, titoli) */
--accent-purple: #7c3aed;   /* Viola (gradiente, CTA) */
--text-primary: #f0f6fc;    /* Testo principale */
--text-secondary: #94a3b8;  /* Testo secondario/commenti */
```

### Colori Semantici
```css
--success: #4ade80;         /* Verde (opportunità, successo) */
--warning: #fbbf24;         /* Giallo (attenzione, medio) */
--danger: #ef4444;          /* Rosso (errori, alto rischio) */
--info: #3b82f6;           /* Blu info */
```

---

## 📏 **Typography Scale Aggiornata - V1.1**

### Font Sizing Philosophy
- **Approccio**: Font più piccoli con interlinea generosa per eleganza e leggibilità
- **Spazio negativo**: Priorità agli spazi bianchi per respirabilità del layout
- **Densità informativa**: Ridotta per migliorare UX

### Nuova Scala Tipografica
```css
/* Base Typography */
body: 0.875rem (14px) - line-height: 1.8
p: 0.875rem (14px) - line-height: 1.8 - margin-bottom: 1.5rem
.lead: 1rem (16px) - line-height: 1.7 - margin-bottom: 2rem

/* Headers Ridimensionate */
h1 (.header-gradient): 2.5rem (40px) - line-height: 1.3 - margin-bottom: 2rem
h2 (.section-title): 1.75rem (28px) - line-height: 1.4 - margin-bottom: 3rem
h3 (.keyword-card h3): 1rem (16px) - line-height: 1.5 - margin-bottom: 1rem

/* Small Text */
.table td, th: 0.8rem (12.8px) - line-height: 1.6
.keyword-card content: 0.8rem (12.8px) - line-height: 1.7
.form-label: 0.8rem (12.8px) - letter-spacing: 0.3px
```

### Spacing Migliorato
```css
/* Padding Aumentato */
.section-card: padding: 3.5rem (56px) - margin-bottom: 3rem
.keyword-card: padding: 2rem (32px) - margin-bottom: 1.5rem
.container: padding-left/right: 2rem (32px)
.container-fluid: padding-top/bottom: 4rem (64px)

/* Table Spacing */
.table td, th: padding: 1rem 1.5rem (16px 24px)
.table th: padding-top/bottom: 1.25rem (20px)

/* Button Spacing */
.btn: padding: 0.75rem 2rem (12px 32px)
```

### Mobile Responsive Adjustments
```css
@media (max-width: 768px) {
    .section-card: padding: 2.5rem 2rem
    .header-gradient: font-size: 2rem
    .section-title: font-size: 1.5rem
    .container: padding-left/right: 1.5rem
}
```

---

## 🎯 **Design Rationale V1.1**

### Perché Font Più Piccoli?
1. **Eleganza moderna**: Look più raffinato e professionale
2. **Densità controllata**: Meno sovraccarico visivo
3. **Gerarchia chiara**: Contrasti di dimensione più sottili ma efficaci
4. **Mobile-friendly**: Migliore adattamento su schermi piccoli

### Perché Interlinea Maggiore?
1. **Leggibilità superiore**: Testo più facile da scansionare
2. **Respiro visivo**: Meno affollamento, più eleganza
3. **Professionalità**: Tipografia da pubblicazione di qualità
4. **Accessibilità**: Migliore per utenti con difficoltà di lettura

### Perché Padding Maggiore?
1. **Spazio negativo**: Elemento fondamentale del design moderno
2. **Focus sul contenuto**: Meno distrazioni, più concentrazione
3. **Breathing room**: Layout che "respira" è più piacevole
4. **Premium feel**: Design che comunica qualità e attenzione ai dettagli

---

## 📐 **Layout e Spacing**

### Container e Griglia
- **Container**: Bootstrap container standard
- **Padding**: `py-5` per sezioni principali
- **Margin**: `mb-5` tra sezioni
- **Gap**: `g-4` per row grids

### Cards e Componenti
```css
.section-card {
    background: #161b22;
    border: 1px solid #30363d;
    border-radius: 15px;
    padding: 2.5rem;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
}
```

### Spacing Scale
- **xs**: 0.25rem (4px)
- **sm**: 0.5rem (8px)
- **md**: 1rem (16px)
- **lg**: 1.5rem (24px)
- **xl**: 2rem (32px)
- **2xl**: 2.5rem (40px)

---

## 🎭 **Componenti UI**

### Buttons
```css
/* Primary Button */
.btn-primary {
    background: linear-gradient(45deg, #58a6ff, #7c3aed);
    border: none;
    font-weight: 500;
    transition: all 0.3s ease;
}

/* Hover Effect */
.btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(88, 166, 255, 0.3);
}
```

### Cards
- **Border radius**: 12-15px
- **Border**: 1px solid #30363d
- **Hover**: Transform translateY(-3px to -5px)
- **Box shadow**: Sempre presente, intensificata su hover

### Tables
- **Background**: #161b22
- **Headers**: #58a6ff background
- **Hover rows**: #21262d background
- **Border**: #30363d

---

## ✨ **Animazioni e Transizioni**

### Timing
- **Standard**: `transition: all 0.3s ease;`
- **Hover lift**: `transform: translateY(-2px to -5px);`
- **Box shadow**: Sempre animated

### Hover Effects
1. **Cards**: Lift + border color change + shadow intensification
2. **Buttons**: Lift + gradient shift + glow
3. **Images**: Subtle lift + shadow

### Micro-interazioni
- **Smooth scrolling**: Abilitato
- **Progressive disclosure**: Cards si aprono/chiudono
- **Loading states**: Skeleton o fade-in

---

## 📱 **Responsive Design**

### Breakpoints Bootstrap
- **xs**: <576px
- **sm**: ≥576px
- **md**: ≥768px (tablet)
- **lg**: ≥992px (desktop)
- **xl**: ≥1200px
- **xxl**: ≥1400px

### Mobile Adjustments
```css
@media (max-width: 768px) {
    .section-card {
        padding: 1.5rem;        /* Riduzione padding */
        margin-bottom: 1.5rem; 
    }
    
    .display-4 {
        font-size: 2.5rem;      /* Headers più piccoli */
    }
}
```

---

## 🏗️ **Struttura HTML Standard**

### Template Base
```html
<!DOCTYPE html>
<html lang="it" data-bs-theme="dark">
<head>
    <!-- Bootstrap 5 + JetBrains Mono + Custom CSS -->
</head>
<body>
    <div class="container-fluid py-5">
        <div class="container">
            <header class="text-center mb-5">
                <h1 class="header-gradient">Title</h1>
            </header>
            
            <section class="section-card mb-5">
                <h2 class="section-title">Section</h2>
                <!-- Content -->
            </section>
        </div>
    </div>
</body>
</html>
```

### Classi CSS Comuni
- `.header-gradient`: Titoli con gradiente
- `.section-card`: Cards principali
- `.section-title`: Titoli sezioni
- `.keyword-card`: Cards secondarie
- `.code-accent`: Testo con accent color
- `.code-comment`: Testo stile commento
- `.opportunity-high/medium/low`: Colori semantici opportunità

---

## 🔧 **Best Practices**

### CSS
1. **Mobile-first**: Partire da mobile, poi desktop
2. **BEM naming**: Dove possibile per custom classes
3. **Custom properties**: Usare CSS variables per colori
4. **Consistent spacing**: Usare scale definita
5. **Performance**: Limitare box-shadows complesse

### HTML
1. **Semantic markup**: Header, section, article, aside
2. **Accessibility**: Alt text, ARIA labels dove necessario
3. **Bootstrap grid**: Sempre responsive
4. **Clean structure**: Indentazione consistente

### JavaScript
1. **Progressive enhancement**: Funziona senza JS
2. **Event delegation**: Per performance
3. **Smooth interactions**: Mai abrupt changes
4. **Error handling**: Graceful fallbacks

---

## 🎯 **Applicazione per Progetti**

### Homepage Portfolio
- **Hero section**: Full viewport height
- **Project cards**: Grid responsive con hover effects
- **Navigation**: Smooth scroll interno

### Progetti Individuali
- **Consistent theming**: Stessi colori e font
- **Content focus**: Typography leggibile
- **Data visualization**: Tables e charts con stesso stile

### Futuro
- **Dark/Light toggle**: Preparare variabili CSS
- **Component library**: Riutilizzare componenti
- **Animation library**: Considerare Framer Motion o simili

---

## 📋 **Checklist Applicazione**

### Per Ogni Nuovo Progetto:
- [ ] Bootstrap 5 + JetBrains Mono inclusi
- [ ] Palette colori rispettata
- [ ] Hover effects implementati
- [ ] Responsive verificato su mobile
- [ ] Accessibility basics verificate
- [ ] Loading performance ottimizzata
- [ ] Smooth scrolling abilitato
- [ ] Footer con stile consistente

### QA Design:
- [ ] Contrasti colori accessibili
- [ ] Font size leggibile su mobile
- [ ] Buttons sufficientemente grandi per touch
- [ ] Spacing consistente
- [ ] Animazioni non troppo aggressive
- [ ] Cross-browser compatibility

---

**Ultimo aggiornamento**: 18 Giugno 2025  
**Versione Design System**: 1.0.0
