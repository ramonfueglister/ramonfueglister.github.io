# ramonfueglister.github.io

Persönliche Homepage von Ramon Füglister – erstellt mit [Astro](https://astro.build), gehostet auf GitHub Pages.

## Lokal entwickeln

```bash
npm install
npm run dev
```

Die Seite läuft dann auf http://localhost:4321 und lädt bei Änderungen automatisch neu.

Weitere Befehle:

| Befehl            | Aktion                                         |
| ----------------- | ---------------------------------------------- |
| `npm run build`   | Baut die statische Seite nach `dist/`          |
| `npm run preview` | Testet den Build lokal                         |

## Inhalte anpassen

Alle Texte stehen in **`src/pages/index.astro`** – die Platzhalter sind mit
`TODO`-Kommentaren markiert:

- Hero: Untertitel & Einleitung
- Über mich: Text
- Lebenslauf: Arrays `berufserfahrung` und `ausbildung`
- Projekte: Array `projekte`
- Kontakt: Variable `email` und Array `socials`

Das Design ist bewusst minimal: weisser Grund, klare Typografie, ein ruhiges
Raster und Blau als präziser Akzent. Globale Farben, Schriften und Navigation
stehen in `src/layouts/Base.astro`; Seiteninhalt und Abschnittsgestaltung in
`src/pages/index.astro`.

## Deployment auf GitHub Pages

Einmalig einrichten:

1. Auf GitHub ein Repository mit dem exakten Namen **`ramonfueglister.github.io`** erstellen (public).
2. Das lokale Repo verbinden und pushen:

   ```bash
   git add .
   git commit -m "Initial commit: Astro homepage"
   git remote add origin git@github.com:ramonfueglister/ramonfueglister.github.io.git
   git push -u origin master
   ```

3. Im GitHub-Repo: **Settings → Pages → Source: "GitHub Actions"** auswählen.

Danach deployed der Workflow in `.github/workflows/deploy.yml` bei jedem
Push auf `master` automatisch. Die Seite ist dann unter
**https://ramonfueglister.github.io** erreichbar.
