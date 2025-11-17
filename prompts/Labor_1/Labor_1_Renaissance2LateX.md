Erstelle ein LaTeX-Dokument zum Thema "Modal Harmony in Renaissance Music"

**Projekt-Setup:**
- Titel: Modal Harmony in Renaissance Music
- Untertitel: An Introduction through the Dorian Mode
- Autor: Author
- Sprache: English
- Format: LaTeX (direkt in Overleaf kompilierbar mit pdfLaTeX)
- Seiten: 2-3 Seiten

**Quellen (mit web_fetch laden):**
- https://www.earlymusicsources.com/youtube/modes
- https://en.wikipedia.org/wiki/Gregorian_mode
- https://gregorian-chant-hymns.com (Um Gregorianische Choräle zu verlinken, mit Audio Beispielen)
- Knud Jeppesen, Counterpoint: The Polyphonic Vocal Style of the Sixteenth Century
- Knud Jeppesen, The Style of Palestrina and the Dissonance
- Bernhard Meier, Alte Tonarten (Baerenreiter)

**Layout & Design:**
- Verwende folgende packages um ein farbiges Dokument zu erstellen:
  - \usepackage{graphicx}
  - \usepackage{xcolor}
  - \usepackage[most]{tcolorbox}
  - \usepackage{tikz}
  - \usepackage{pgfornament}
  - \usepackage{fancyhdr}
  - \usepackage{lettrine}
  - \usepackage{musixtex}  % Musiknotation
- Color Scheme:
  * Primary: RGB(139,69,19) - Renaissance Brown
  * Secondary: RGB(184,134,11) - Gold
  * Accent: RGB(128,0,0) - Deep Red
- Geometry: [left=2.5cm,right=2.5cm,top=3cm,bottom=3cm,headheight=24pt]
- Verwende Header, Color Boxes, Ornament-Dividers, TikZ-Diagramme bei Bedarf 
- Fußnoten für Quellenangaben

**Wichtige LaTeX-Regeln:**
- Musikbeispiele als MusiXTeX oder als EInbindung von png
- Format: \includegraphics[width=0.8\textwidth]{dateiname.png}
- Caption mit Beschreibung statt inline-Notation
- Verwende KEINE Unicode-Musiksymbole (♭, ♯, ♮)
- Accidentals nur in Math-Mode: $\flat$, $\sharp$, $\natural$
- Römische Stufensymbole: Verwende \textbf{i}, \textbf{iv}, \textbf{v} für Moll-Stufen
  * Beispiel: \textbf{i}--\textbf{iv}--\textbf{v}--\textbf{i} für eine Moll-Progression
- MusiXTeX:
  - MusiXTeX Vorzeichen: _d (D-flat), ^d (D-sharp), =d (D-natural)
  - MusiXTeX Oktaven: d (mittel), d' (hoch), d` (tief)

**Section 1: Introduction to Modal Theory**
- Was ist der Dorische Modus? (8-10 Zeilen)
- Historischer Kontext (Renaissance, Gregorianik)
- Verwende \lettrine am Anfang
- TikZ-Diagramm der Dorian Scale Struktur
- Tcolorbox: "The Dorian Mode"
  * Formula: 1-2-$\flat$3-4-5-6-$\flat$7-8
  * In D: D E F G A B C D
  * Charakteristik: Minor 3rd, Major 6th

**Musikbeispiel 1: Literaturbeispiel (MusiXTeX)**
- "Veni Creator Spiritus" (Gregorianischer Hymnus, Dorian)
- MusiXTeX inline notation
- 1 System, Violin Clef, 4-8 Takte
- Noten: D E F G A B C D... (authentisches Beispiel)
- Kurze Analyse (3-4 Zeilen): Finalis auf D, modale Kadenz

**Musikbeispiel 2: Variatio von Ferdinand Richardson**
- Füge das PNG-Bild als Platzhalter ein: "Variatio_Richardson.png"
- Quelle: Fitzwilliam Virginal Book I, [genaue Nummer]
- Tonart: [D Dorian / andere]
- Kurze Entstehungsgeschichte (2-3 Zeilen): Kontext des Fitzwilliam Virginal Book
- Harmonische Eigenheiten der englischen Virginalisten (3-4 Zeilen): 
  * Falsche Relationen, modale Mixtur
  * Keine funktionale Harmonik, freie Dissonanzbehandlung
  * Variationstechnik über ostinate Bässe

**MusiXTeX Spezifikationen:**
- Beispiel 1: Einstimmig, Violinschlüssel, whole/half notes
- Beispiel 2: Zweistimmig mit \instrumentnumber{1}\setstaffs{1}{2}
  * Oberes System: Treble Clef (Akkorde als \zqu{...}\qu{...})
  * Unteres System: Bass Clef (Grundtöne)
- Vollständig ausnotiert, NICHT als Platzhalter!

**Practice Strategies:**
- Tcolorbox: "Practice Tips"
  * Sing the Dorian scale 
  * Play progression in all keys
  * Listen to Gregorian chant recordings

**WICHTIG:**
- Kompiliere mit pdfLaTeX (NICHT latex/DVI)
- MusiXTeX Code direkt im Dokument einbetten
- Bei Verwendung externer Quellen: Fußnoten mit Verlinkung ins Literaturverzeichnis
- Verwende pgfornament Dividers zwischen Sektionen