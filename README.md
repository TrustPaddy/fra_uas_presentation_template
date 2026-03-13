# FRA UAS HTML-Präsentationstemplate

Ein modernes, browserbasiertes Präsentationstemplate gedacht für Studierende der **Frankfurt University of Applied Sciences** (aber auch mit anderen Templates kompatibel) und entwickelt für Ingenieurstudiengänge und Informatik.

---

## Was ist das?

Diese Datei (`template.html`) ist ein vollständig eigenständiges Präsentationstemplate, das direkt im Browser läuft. Es basiert auf [Reveal.js](https://revealjs.com/) und enthält eine umfangreiche Sammlung an vorgefertigten Folientypen – von einfachen Aufzählungen bis hin zu interaktiven Visualisierungen, die mit PowerPoint so nicht umsetzbar wären.

---

## Zweck

Das Template dient als Ausgangspunkt für Seminar-, Projekt- und Abschlussarbeitspräsentationen. Es enthält das Corporate-Design der Frankfurt UAS (Logo, Hintergrundbilder, Farbschema) und ist auf wissenschaftliche Inhalte aus Ingenieurwesen und Informatik zugeschnitten. Je nach Bedarf ist das Design aber beliebig anpassbar durch austauschen der dateien, beispielsweise wenn die Präsentation für eine andere Einrichtung gedacht ist. Dazu müssen lediglich die Bilder „bg_xxx.png” durch eigene Designs ersetzt werden.   

---

## Für wen ist das gedacht?

Primär für Studierende aus:

- **Mechatronik / Maschinenbau** – Systemmodelle, Regelungstechnik, Simulationen
- **Informatik / Elektrotechnik** – Algorithmen, Code, Architekturen, Datenvisualisierung
- **Ingenieurwissenschaften allgemein** – Formeln, Messkurven, Vergleichstabellen

Aber auch für alle anderen, die eine professionelle, animierte Präsentation im Browser erstellen möchten.

---

## Vorteile gegenüber PowerPoint

| Merkmal | PowerPoint | Dieses Template |
|---------|-----------|-----------------|
| Code-Darstellung | Nur Text, kein Highlighting | Syntax-Highlighting (Python, C++, ...) |
| Mathematik | Umständlicher Formeleditor | KaTeX – LaTeX-Syntax direkt im HTML |
| Animationen | Vorgefertigte Effekte | Beliebige CSS/JS-Animationen |
| Live-Graphen | Nicht möglich | Canvas-API, SVG, D3 – alles möglich |
| Terminal-Simulation | Nicht möglich | Typewriter-Effekt im Dark-Mode |
| Versionierung | Schwierig (binäres Format) | Plaintext-HTML → perfekt für Git |
| Portabilität | .pptx, Software erforderlich | Einzelne .html-Datei, kein Install |
| Anpassbarkeit | Begrenzt | Vollständige Kontrolle über CSS/JS |
| Reproduzierbarkeit | OS- und Versionsabhängig | Gleicher Output in jedem Browser |

---

## Quickstart

### 1. Dateien vorbereiten

Stelle sicher, dass folgende Dateien im gleichen Ordner liegen:

```
template.html        ← Das Template (diese Datei bearbeiten)
fra_uas_logo.png     ← FRA UAS Logo
bg_title.png         ← Hintergrund Titelfolie
bg_content.png       ← Hintergrund Inhaltsfolien
bg_end.png           ← Hintergrund Danke-Folie
```

### 2. Platzhalter ersetzen

Suche in `template.html` nach allen Stellen mit `[...]` und ersetze sie:

| Platzhalter | Ersetzen durch |
|-------------|---------------|
| `[TITEL DER PRÄSENTATION]` | Deinen Präsentationstitel |
| `[Untertitel oder Themenfeld]` | Untertitel (optional) |
| `[Modul / Seminar / Projektbezeichnung]` | z.B. „Mechatronikprojekt" |
| `[Vorname Nachname]` | Deinen vollständigen Namen |
| `[XXXXXXX]` | Deine Matrikelnummer |
| `[Studiengang]` | z.B. „Informatik" oder „Mechatronik" |
| `[B.Eng. / M.Eng. / ...]` | Deinen Abschluss |
| `[Titel Vorname Nachname]` | Name deines Betreuers |
| `[TT. Monat JJJJ]` | Datum der Präsentation |
| `[DATUM]` im Footer | Kurzes Datum im Folien-Footer |
| `[MODUL]` im Footer | Modulname im Folien-Footer |
| `[NAME]` im Footer | Dein Name im Folien-Footer |

### 3. Im Browser öffnen

Öffne `template.html` einfach per Doppelklick in **Chrome** oder **Firefox**.

**Navigation:**
- `→` / `←` – Folien vor/zurück
- `F` – Vollbild
- `S` – Sprechernotizen (falls vorhanden)
- `Esc` – Übersicht aller Folien

### 4. Präsentieren

Im Vollbild-Modus (`F`) läuft die Präsentation wie eine normale Slide-Show.
Für Beamer empfiehlt sich Chrome im Vollbild.

---

## Verwendung mit KI (empfohlener Workflow)

Das Template ist so gestaltet, dass du es effizient mit KI-Assistenten wie **Claude**, **ChatGPT** oder **GitHub Copilot** befüllen kannst.

### Beispiel-Prompts

**Inhalte generieren lassen:**
```
Ich halte eine Präsentation über [THEMA] im Studiengang [STUDIENGANG]
an der Frankfurt UAS. Befülle Folie 4 (Motivation & Problemstellung)
aus template.html mit sinnvollen Inhalten zu meinem Thema.
Behalte die HTML-Struktur exakt bei.
```

**Neue Folie erstellen:**
```
Erstelle eine neue Folie für template.html im Stil von Folie 9
(Code-Block), aber mit diesem Python-Code: [CODE EINFÜGEN].
Titel: "Implementierung des Kalman-Filters"
```

**Balkendiagramm anpassen:**
```
Passe das Balkendiagramm auf Folie 8 in template.html an.
Ich habe folgende Messwerte: PPO=94%, SAC=87%, TD3=79%, DDPG=65%.
Passe Balkenfarben, Labels und data-height-Werte entsprechend an.
```

**Formeln einfügen:**
```
Füge auf Folie 11 (Mathematisches Modell) eine weitere Gleichungsbox
hinzu mit der Kalman-Filter-Update-Gleichung in LaTeX-Syntax.
```

### Tipps für beste Ergebnisse

- **Zeige der KI immer den vollständigen HTML-Block der Zielfolie** – so kann sie die Struktur korrekt beibehalten
- **Gib deine Daten (Messwerte, Code, Formeln) direkt mit** – die KI soll nur die Präsentation formatieren, nicht die Inhalte erfinden
- **Lass Folien schrittweise befüllen** – eine Folie pro Prompt liefert bessere Ergebnisse als alle auf einmal
- Animationen (★-Folien) funktionieren ohne Anpassung – nur Labels und Daten müssen geändert werden

---

## Technische Details

Das Template verwendet ausschließlich CDN-Libraries – keine lokale Installation erforderlich:

- **Reveal.js 4.6.1** – Präsentations-Framework
- **KaTeX 0.16.9** – LaTeX-Matheformel-Rendering
- **Highlight.js 11.9** – Syntax-Highlighting (Python, C++, JavaScript, ...)
- **Inter & Fira Code** – Google Fonts
- Alle Animationen: pure CSS + vanilla JavaScript


