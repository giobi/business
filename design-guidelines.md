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

## 🔤 **Tipografia**

### Font Principal
- **Font**: JetBrains Mono (monospace)
- **Pesi**: 300, 400, 500, 600, 700
- **Uso**: Tutto il testo per consistenza "developer"

### Gerarchia Tipografica
```css
/* Headers */
h1: 3.5rem (display-4) - fw-bold
h2: 2.5rem (section-title) - fw-600
h3: 1.5rem (card-title) - fw-600
h4: 1.25rem (subtitle) - fw-500

/* Body */
p: 1rem (base) - fw-400
small: 0.875rem - fw-400
```

### Stili Speciali
- **Code Accent**: `color: #58a6ff; font-weight: 500;`
- **Comments**: `color: #94a3b8; font-style: italic;`
- **Gradients**: Effetto testo trasparente con gradiente

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
