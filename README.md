# Test-Projekt - Einfache GitHub Pages Website

Eine einfache, responsive Website, die mit HTML und CSS erstellt wurde und für die Bereitstellung auf GitHub Pages konzipiert ist.

## 🌟 Funktionen

- Sauberes, responsives Design
- Modernes CSS mit Farbverlaufshintergründen
- Sanfte Scroll-Navigation
- Mobilfreundliches Layout
- Einfach anzupassen und zu erweitern

## 🚀 Live-Demo

Nach der Bereitstellung wird Ihre Website unter folgender Adresse verfügbar sein: `https://[ihr-benutzername].github.io/[repository-name]`

## 📁 Projektstruktur

```
test-project/
├── index.html      # Haupt-HTML-Datei
├── styles.css      # CSS-Styling
└── README.md       # Diese Datei
```

## 🛠️ Bereitstellung auf GitHub Pages

### Methode 1: Verwendung der GitHub-Weboberfläche (Empfohlen)

1. **Code zu GitHub hochladen** (falls noch nicht geschehen):
   ```bash
   git add .
   git commit -m "Add simple GitHub Pages website"
   git push origin main
   ```

2. **GitHub Pages aktivieren**:
   - Gehen Sie zu Ihrem Repository auf GitHub
   - Klicken Sie auf den **Settings**-Tab
   - Scrollen Sie nach unten zum **Pages**-Bereich in der linken Seitenleiste
   - Unter **Source** wählen Sie **Deploy from a branch**
   - Wählen Sie den **main**-Branch und den **/ (root)**-Ordner
   - Klicken Sie auf **Save**

3. **Auf Ihre Website zugreifen**:
   - GitHub stellt eine URL bereit wie: `https://[ihr-benutzername].github.io/[repository-name]`
   - Es kann einige Minuten dauern, bis die Seite verfügbar ist

### Methode 2: Verwendung von GitHub Actions (Fortgeschritten)

1. Erstellen Sie `.github/workflows/pages.yml`:
   ```yaml
   name: Deploy to GitHub Pages

   on:
     push:
       branches: [ main ]

   jobs:
     deploy:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - name: Deploy to GitHub Pages
           uses: peaceiris/actions-gh-pages@v3
           with:
             github_token: ${{ secrets.GITHUB_TOKEN }}
             publish_dir: ./
   ```

2. Laden Sie die Workflow-Datei hoch und Ihre Seite wird bei jedem Push automatisch bereitgestellt.

## 🔧 Lokale Entwicklung

Um Ihre Website lokal zu testen:

1. **Einfacher HTTP-Server** (Python):
   ```bash
   # Python 3
   python -m http.server 8000

   # Python 2
   python -m SimpleHTTPServer 8000
   ```
   Öffnen Sie dann `http://localhost:8000`

2. **Live Server** (VS Code-Erweiterung):
   - Installieren Sie die "Live Server"-Erweiterung
   - Rechtsklick auf `index.html`
   - Wählen Sie "Open with Live Server"

3. **Node.js http-server**:
   ```bash
   npx http-server
   ```

## 🎨 Anpassung

### Farben ändern
Bearbeiten Sie die CSS-Variablen in `styles.css`:
- Header-Verlauf: `linear-gradient(135deg, #667eea 0%, #764ba2 100%)`
- Akzentfarben: `#667eea` und `#764ba2`

### Inhalte hinzufügen
- Ändern Sie Abschnitte in `index.html`
- Fügen Sie neue Seiten hinzu, indem Sie zusätzliche `.html`-Dateien erstellen
- Aktualisieren Sie die Navigationslinks im Header

### Bilder hinzufügen
1. Erstellen Sie einen `images/`-Ordner
2. Fügen Sie Ihre Bilder zum Ordner hinzu
3. Referenzieren Sie sie im HTML: `<img src="images/ihr-bild.jpg" alt="Beschreibung">`

## 📱 Responsives Design

Die Website enthält responsive Design-Funktionen:
- Mobilfreundliche Navigation
- Flexibles Grid-Layout
- Skalierbare Typografie
- Berührungsfreundliche Schaltflächen

## 🔗 Eigene Domain (Optional)

Um eine eigene Domain zu verwenden:

1. Erstellen Sie eine `CNAME`-Datei im Stammverzeichnis mit Ihrer Domain:
   ```
   ihredomain.com
   ```

2. Konfigurieren Sie DNS-Einträge bei Ihrem Domain-Anbieter:
   - Fügen Sie einen CNAME-Eintrag hinzu, der auf `[ihr-benutzername].github.io` zeigt

3. Aktualisieren Sie die GitHub Pages-Einstellungen, um Ihre eigene Domain zu verwenden

## 📝 Fehlerbehebung

**Seite lädt nicht?**
- Warten Sie 5-10 Minuten nach der Aktivierung von GitHub Pages
- Überprüfen Sie, dass sich `index.html` im Stammverzeichnis befindet
- Stellen Sie sicher, dass das Repository öffentlich ist (oder Sie haben GitHub Pro für private Repos)

**Änderungen werden nicht angezeigt?**
- Browser-Cache leeren
- Warten Sie einige Minuten, bis GitHub die Seite neu erstellt
- Überprüfen Sie den Actions-Tab für den Build-Status

**Probleme mit eigener Domain?**
- DNS-Propagation überprüfen (kann bis zu 24 Stunden dauern)
- CNAME-Dateiformat überprüfen (kein `http://` oder `https://`)

## 📄 Lizenz

Dieses Projekt ist Open Source und unter der [MIT-Lizenz](LICENSE) verfügbar.

## 🤝 Mitwirkung

Forken Sie gerne dieses Projekt und reichen Sie Pull Requests für Verbesserungen ein!
