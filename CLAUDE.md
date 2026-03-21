# LAUNCH-LOTSE

## Projektübersicht

Der Launch-Lotse ist eine Landingpage, die die Bedienung der Startrampe erklärt. Er führt Benutzer durch die Voraussetzungen und den Ablauf des Deployment-Prozesses — bevor sie die Startrampe selbst öffnen.

**Subdomain:** `launch-lotse.berent.ai`
**Repository:** `peerendees/launch-lotse`
**Typ:** Öffentliche Informationsseite (für Workshop-Teilnehmer und Kunden)
**Schwester-Projekt:** Startrampe (`startrampe.berent.ai`, Repo `peerendees/startrampe`)

## Architektur

- **Single-File Frontend:** `index.html` — gesamte App (HTML, CSS, JS) in einer Datei
- **Kein Backend:** Rein statische Seite
- **Kein Build-Prozess:** Keine npm-Dependencies

## Technologie-Stack

| Bereich | Technologie |
|---------|-------------|
| Frontend | Vanilla HTML/CSS/JS (kein Framework) |
| Fonts | Lokal gehostet: Bebas Neue, Lora, JetBrains Mono |
| Deployment | Vercel (statisch) |

## Zielgruppen und Niveaus

Die Seite unterstützt zwei Erfahrungsniveaus via Toggle:

### Einsteiger
- Braucht GitHub-Konto, Vercel-Konto, Cloudflare-Konto
- Ausführliche Erklärungen, was jeder Dienst tut
- Checkliste mit Direkt-Links zur Kontoerstellung
- Hinweis-Boxen mit Zusatzinfos

### Fortgeschritten
- Hat bereits alle Konten
- Kompakte Darstellung ohne Erklärungen
- Fokus auf den Ablauf

## Inhaltliche Struktur

1. **Hero** — Titel, Tagline, CTA-Button zur Startrampe
2. **Was ist die Startrampe?** — Feature-Grid (Personalisiert, Copy-Paste, Privat, 15 Min.)
3. **Was brauchst du?** — Voraussetzungen-Checkliste (niveau-abhängig)
4. **So funktioniert es** — 6-Schritte-Ablauf
5. **Was du eingeben musst** — Die 4 Pflichtfelder erklärt
6. **Für wen?** — Zielgruppen-Grid
7. **CTA** — Abschluss-Box mit Link zur Startrampe

## Corporate Identity — BERENT.AI

Die Seite folgt der BERENT.AI CI, orientiert am Textschmiede-Stil:

- **Farben:** `--bg: #090806`, `--surface: #110e0a`, `--copper: #B5742A`, `--gold: #E8C98A`
- **Typografie:** Bebas Neue (Headlines, uppercase), Lora (Fließtext, font-weight 300), JetBrains Mono (Labels, Code)
- **Fonts DSGVO-konform lokal gehostet** — kein Google Fonts CDN
- **Plus-Symbol:** Obligatorisches Markenelement in Header, Section-Titeln und Hero
- **Grain-Overlay und Glow-Orb:** Wie bei der Textschmiede (body::before und body::after)
- **Scroll-Animationen:** Sections faden beim Scrollen ein (IntersectionObserver)
- **Kein Ampersand:** In UI-Texten immer „und" statt „&"
- **Footer-Pflichtlinks:** Impressum + berent.ai

## Vorbilder

| Aspekt | Vorbild | Was übernommen |
|--------|---------|----------------|
| Einstieg und Stil | Textschmiede (`textschmiede-5tc.berent.ai`) | Hero mit Plus-Symbol, Grain-Overlay, Section-Cards mit abgerundeten Ecken, Scroll-Animationen |
| Inhaltlicher Ton | Relaunch Guide (`relaunch-guide.berent.ai`) | Erklärender Guide-Charakter |

## Dateien

```
index.html              # Komplette Landingpage
vercel.json             # Vercel-Konfiguration
CLAUDE.md               # Diese Datei — Projektdokumentation
assets/
  fonts/                # Lokal gehostete Fonts (Bebas Neue, Lora, JetBrains Mono)
  images/
    logo_farbe_v3.webp  # BERENT Wortschriftzug
    BE_Farbe_V3.png     # BERENT Signet (Favicon, PNG)
    BE_Farbe_V3.webp    # BERENT Signet (Favicon, WebP)
.claude/
  launch.json           # Dev-Server-Konfiguration
```

## Konventionen

- **Sprache der UI:** Deutsch
- **Commit-Sprache:** Englisch
- **CSS:** Custom Properties in `:root`, keine Preprocessoren
- **JS:** Vanilla JS, keine Module, globale Funktionen
- **Naming:** camelCase (JS), kebab-case (CSS)
- **Kein Ampersand:** `&` niemals als Konjunktion in UI-Texten
- **Alle Änderungen** betreffen primär `index.html`

## Beziehung zur Startrampe

- Der Launch-Lotse **beschreibt** die Startrampe, er **ist** nicht die Startrampe
- CTA-Buttons verlinken auf `startrampe.berent.ai`
- Die Inhalte müssen mit dem tatsächlichen Ablauf der Startrampe übereinstimmen
- Änderungen an der Startrampe (neue Schritte, geänderte Felder) erfordern Aktualisierung des Launch-Lotsen
