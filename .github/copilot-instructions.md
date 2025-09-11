# Giobicom25 Portfolio - GitHub Copilot Instructions

**ALWAYS follow these instructions first** and only search for additional context if the information here is incomplete or found to be in error.

## Project Overview

Giobicom25 is a **static HTML portfolio website** showcasing projects developed in 2025. It uses Bootstrap 5 with a dark theme, JetBrains Mono font, and is designed for modern web browsers with responsive design principles.

**Technology Stack:**
- Pure HTML5, CSS3, JavaScript
- Bootstrap 5.3.2 (loaded via CDN)
- JetBrains Mono font (Google Fonts CDN)
- No build system or package manager required
- No external dependencies to install

## Repository Structure

```
/
├── index.html              # Main portfolio homepage
├── README.md               # Project documentation
├── design-guidelines.md    # Comprehensive design system guide
├── Export_prodotti.xlsx    # Excel file (products export)
├── project/                # Individual project directories
│   └── stresasalute.it/   # Stresa Salute project
│       ├── index.html     # Project homepage
│       ├── index-new.html # Alternative version
│       ├── css/           # Project-specific CSS
│       └── img/           # Project images
├── quote/                  # Project quotes and documentation
│   ├── quotes-2025.pdf    # PDF quotes
│   └── readme.md          # Quote documentation
├── template/               # HTML templates
│   └── mountain.html      # Mountain theme template
└── note/                   # Project notes
    └── 2025.md            # 2025 development notes
```

## Development Workflow

### Initial Setup
Run these commands to get started with development:

```bash
# Clone repository (if not already done)
git clone <repository-url>
cd business

# Validate HTML syntax
python3 -c "
import html.parser
with open('index.html', 'r', encoding='utf-8') as f:
    content = f.read()
parser = html.parser.HTMLParser()
parser.feed(content)
print('✓ HTML syntax is valid')
"
```

### Local Development Server
Start a local development server to preview changes:

```bash
# Start HTTP server (takes ~2 seconds to start)
cd /home/runner/work/business/business
python3 -m http.server 8080

# Alternative with Node.js (if available)
npx http-server -p 8080

# Alternative with PHP (if available)
php -S localhost:8080
```

**Expected timing:** Server starts in ~2 seconds, no build time required.

Access the site at: `http://localhost:8080`

### File Validation
Always validate your changes before committing (takes ~0.02 seconds):

```bash
# Validate main HTML file
python3 -c "
import html.parser
import sys
try:
    with open('index.html', 'r', encoding='utf-8') as f:
        content = f.read()
    parser = html.parser.HTMLParser()
    parser.feed(content)
    print('✓ HTML syntax is valid')
except Exception as e:
    print(f'✗ HTML validation failed: {e}')
    sys.exit(1)
"

# Check file structure
file index.html  # Should output: HTML document, Unicode text, UTF-8 text

# Verify project images exist
find project/ -name "*.jpg" -o -name "*.png" -o -name "*.gif" | head -5
echo "✓ Available images checked"
```

## Testing and Validation

### Manual Testing Scenarios
**ALWAYS run these validation scenarios after making changes:**

1. **Homepage Functionality Test:**
   ```bash
   # Start server and test main page
   cd /home/runner/work/business/business
   python3 -m http.server 8080 &
   sleep 2
   curl -s -I http://localhost:8080/ | head -2
   # Should return: HTTP/1.0 200 OK
   pkill -f "http.server"
   ```

2. **Navigation Test:**
   - Click "Esplora Progetti" button → should scroll to projects section
   - Click "Visualizza" on Stresa Salute project → should load `project/stresasalute.it/`
   - Test responsive design by resizing browser window

3. **Project Page Test:**
   ```bash
   # Test project page loads correctly
   cd /home/runner/work/business/business
   python3 -m http.server 8080 &
   sleep 2
   curl -s -I http://localhost:8080/project/stresasalute.it/ | head -2
   # Should return: HTTP/1.0 200 OK
   pkill -f "http.server"
   ```

### Cross-Browser Compatibility
Test in these browsers (if available):
- Chrome/Chromium ✓
- Firefox ✓  
- Safari ✓
- Edge ✓

**Note:** CDN resources (Bootstrap, Google Fonts) may be blocked in sandboxed environments but the site structure will remain functional.

## Common Development Tasks

### Adding a New Project
1. Create project directory structure:
   ```bash
   mkdir -p project/new-project-name/{css,img}
   ```

2. Create project homepage:
   ```bash
   cp project/stresasalute.it/index.html project/new-project-name/
   # Edit the copied file to customize content
   ```

3. Add project card to main `index.html`:
   - Find the projects section (`<div class="row g-4" id="progetti">`)
   - Copy existing project card structure
   - Update project name, description, and links

4. Add project cover image:
   ```bash
   # Add cover image (recommended: 600x400px, .png or .jpg)
   # Current project uses: studio-dentistico.png, map.png
   cp your-image.png project/new-project-name/img/
   ```

### Modifying Design System
Reference `design-guidelines.md` for:
- Color palette (`--bg-primary: #0d1117`, etc.)
- Typography scale (base: 0.875rem with 1.8 line-height)
- Component styles (buttons, cards, spacing)
- Responsive breakpoints

**Key Design Principles:**
- GitHub Dark Theme inspired colors
- JetBrains Mono font for developer aesthetic
- Generous white space and padding
- Smooth hover animations (0.3s ease)

### Performance Optimization
```bash
# Optimize images (if tools available)
# Note: No build process required, but images should be optimized manually

# Check file sizes
du -sh * | sort -h

# Verify no unused files
find . -name "*.html" -exec grep -l "unused-class" {} \; || echo "No unused classes found"
```

## Important File Locations

### Frequently Modified Files
- `index.html` - Main portfolio page (most common edits)
- `project/stresasalute.it/index.html` - Main project showcase
- `design-guidelines.md` - Design system reference

### Static Assets
- Project images: `project/*/img/*.png` (studio-dentistico.png, map.png)
- CSS: Inline in HTML files + external CSS in `project/stresasalute.it/css/`
- Templates: `template/mountain.html`

### Documentation
- `README.md` - Project overview and features
- `quote/readme.md` - Quote documentation
- `note/2025.md` - Development notes

## Troubleshooting

### Common Issues

**1. "Site not loading locally"**
```bash
# Check if port is already in use
lsof -i :8080
# If busy, use different port
python3 -m http.server 8081
```

**2. "Images not displaying"**
- Verify image paths are relative: `./project/name/img/image.png`
- Check file permissions: `ls -la project/*/img/`
- Ensure images exist: `find project/ -name "*.png" -o -name "*.jpg"`

**3. "Bootstrap styles not loading"**
- CDN may be blocked in sandboxed environments (expected)
- Site functionality remains intact without external CSS
- Core layout uses inline styles as fallback

**4. "Responsive design broken"**
```bash
# Check viewport meta tag exists in HTML head
grep -n "viewport" index.html
# Should return: <meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Network Limitations
In sandboxed environments:
- CDN resources (Bootstrap, Google Fonts) are blocked by firewall
- Site remains functional with inline styles
- External links (GitHub) will not work
- This is expected behavior and documented as limitation

## Quality Checklist

Before committing changes, verify:
- [ ] HTML validation passes
- [ ] Local HTTP server starts and serves content
- [ ] All internal links work correctly
- [ ] Images load properly (or have proper alt text)
- [ ] Responsive design works on different screen sizes
- [ ] No console errors in browser developer tools
- [ ] New projects added to main portfolio page
- [ ] Design system guidelines followed (colors, fonts, spacing)

## Emergency Commands

```bash
# Revert to working state (if changes broke something)
git status
git checkout -- index.html  # Revert main page
git checkout -- project/    # Revert all projects

# Quick syntax check
python3 -c "import html.parser; parser = html.parser.HTMLParser(); parser.feed(open('index.html').read()); print('OK')"

# Verify server functionality
cd /home/runner/work/business/business && python3 -m http.server 8080 &
sleep 2 && curl -s http://localhost:8080/ | head -10
pkill -f "http.server"
```

---

**Last Updated:** September 2025  
**Environment:** Static HTML portfolio, no build system required  
**Expected Development Time:** Changes are immediate, no compilation needed