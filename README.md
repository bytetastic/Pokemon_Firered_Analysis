# 🎮 Feuerrot – Data Science Analyse

Dieses Projekt analysiert die ROM-Daten von **Pokémon Feuerrot (BPRD – Deutsche Version)** mit einem vollständigen Data-Science-Workflow:
Extraktion → Bereinigung → Analyse → Visualisierung

## ⚖️ Rechtliches

Die in diesem Projekt verwendete ROM-Datei wurde vom Originalspielmodul
selbst ausgelesen (Sicherungskopie für den privaten Gebrauch).

- Die ROM-Datei ist **nicht** Teil dieses Repositories
- Es werden ausschließlich **Datenwerte** (Zahlen & Text) extrahiert
- Keine Weitergabe von geschütztem Spielcode, Grafiken oder Musik
- Nutzung ausschließlich zu **privaten Lernzwecken**

> Privates Projekt im Bereich **Data Science / Analyse**

---

## 🎯 Projektziel

Anhand der Rohdaten aus der Pokémon Feuerrot ROM sollen folgende Fragen beantwortet werden:

- Welche Pokémon-Typen dominieren das Spiel?
- Welche Pokémon sind statistisch am stärksten?
- Ist das Spiel fair ausbalanciert?
- Welche Typen sind offensiv/defensiv am vorteilhaftesten?
- Sind seltene Pokémon wirklich selten?

---

## 🗂️ Projektstruktur

```
Pokemon_Firered_Analysis/
│
├── data/                  # Extrahierte Rohdaten (CSV) – nicht im Git!
├── notebooks/             # Jupyter Notebooks
│   └── 01_extraktion.ipynb
├── visualizations/        # Exportierte Grafiken & Charts
├── requirements.txt       # Python-Abhängigkeiten
└── README.md
```

---

## 📦 Verwendete Bibliotheken

| Bibliothek | Zweck |
|---|---|
| `pandas` | Datenverarbeitung |
| `numpy` | Numerische Berechnungen |
| `matplotlib` | Basis-Visualisierungen |
| `seaborn` | Statistische Grafiken |
| `plotly` | Interaktive Visualisierungen |
| `streamlit` | Interaktives Dashboard (optional) |
| `jupyter` | Notebook-Umgebung |

---

## 🗺️ Ablaufplan & Fortschritt

### Die folgende Roadmap wurde mithilfe von Claude.ai erstellt, spontane Anpassungen sind möglich.
### Erledigte Schritte werden parallel zu Code aktualisiert.

### Phase 1 – Extraktion 📦
**Ziel:** Rohdaten aus der ROM in nutzbare Formate überführen

| Schritt | Aufgabe                                                       | Status             |
|---------|---------------------------------------------------------------|--------------------|
| 1.1     | Projektumgebung einrichten (Python, Jupyter, venv)            | ✅ Fertig           |
| 1.2     | ROM-Struktur verstehen (Hex-Offsets, Datenblöcke)             | ✅ Fertig           |
| 1.3a    | Pokémon-Namen extrahieren                                     | ✅ Fertig           |
| 1.3b    | Pokémon-Basiswerte extrahieren (HP, ATK, DEF, …)              | ✅ Fertig  |
| 1.3c    | Pokémon-Typen extrahieren                                     | ‍✅ Fertig |
| 1.3d    | Dataframes von 1.3 zusammenführen                             | ‍✅ Fertig   |
| 1.4     | Move-Daten extrahieren (Stärke, Genauigkeit, Typ)             | ✅ Fertig         |
| 1.5     | Rohdaten als CSV speichern                                    | ✅ Fertig            |

### Phase 2 – Bereinigung 🧹
**Ziel:** Daten konsistent, vollständig und analysierbar machen

| Schritt | Aufgabe | Status |
|---|---|---|
| 2.1 | Fehlende oder fehlerhafte Werte identifizieren | ⏳ Offen |
| 2.2 | Datentypen korrigieren (z.B. Typ-IDs → Typnamen) | ⏳ Offen |
| 2.3 | Duplikate entfernen | ⏳ Offen |
| 2.4 | Tabellen sinnvoll verknüpfen (z.B. Pokémon ↔ Moves ↔ Encounters) | ⏳ Offen |
| 2.5 | Bereinigtes Dataset als neues CSV abspeichern | ⏳ Offen |

### Phase 3 – Analyse 🔍
**Ziel:** Muster, Zusammenhänge und Auffälligkeiten finden

| Schritt | Fragestellung | Status |
|---|---|---|
| 3.1 | Typverteilung – Welche Typen dominieren? Gibt es Lücken? | ⏳ Offen |
| 3.2 | Stärke-Ranking – Welche Pokémon haben die höchsten Gesamtwerte? | ⏳ Offen |
| 3.3 | Stat-Korrelation – Korrelieren z.B. Angriff und Speed? | ⏳ Offen |
| 3.4 | Encounter-Analyse – Sind seltene Pokémon wirklich selten? | ⏳ Offen |
| 3.5 | Typen-Matchup-Matrix – Welcher Typ ist am stärksten / schwächsten? | ⏳ Offen |
| 3.6 | Balancing-Check – Ist das Spiel fair designt? | ⏳ Offen |

### Phase 4 – Visualisierung 📊
**Ziel:** Ergebnisse anschaulich und präsentierbar machen

| Schritt | Visualisierung | Tool | Status |
|---|---|---|---|
| 4.1 | Balkendiagramm der Typverteilung | `matplotlib` | ⏳ Offen |
| 4.2 | Heatmap der Typ-Matchups | `seaborn` | ⏳ Offen |
| 4.3 | Radar-Charts für Pokémon-Stats | `plotly` | ⏳ Offen |
| 4.4 | Top-10 Pokémon nach Gesamtstärke | `seaborn` | ⏳ Offen |
| 4.5 | Encounter-Karte pro Route | `plotly` | ⏳ Offen |
| 4.6 | Interaktives Dashboard (optional) | `streamlit` | ⏳ Offen |

### Phase 5 – Präsentation 👨‍💻
**Ziel:** Projekt dokumentieren und vorstellen

| Schritt | Aufgabe                                  | Status |
|---|------------------------------------------|---|
| 5.1 | Kernaussagen formulieren: „Was wurde herausgefunden?" | ⏳ Offen |

---

## 📅 Projektzeitplan

```mermaid
gantt
    title Feuerrot – Projektzeitplan
    dateFormat  YYYY-MM-DD
    section Phase 1 📦 Extraktion
    Phase 1 – Extraktion     :done,    p1, 2026-03-05, 5d

    section Phase 2 🧹 Bereinigung
    Phase 2 – Bereinigung    :         p2, 2026-03-10, 5d

    section Phase 3 🔍 Analyse
    Phase 3 – Analyse        :         p3, 2026-03-15, 5d

    section Phase 4 📊 Visualisierung
    Phase 4 – Visualisierung :         p4, 2026-03-20, 5d

    section Phase 5 👨‍💻 Präsentation
    Phase 5 – Präsentation   :         p5, 2026-03-25, 4d
```

---

## 📝 Ergebnisse & Erkenntnisse

> *Wird nach Abschluss der Analyse ergänzt.*

---

## ⚠️ Hinweise

- Die ROM-Datei (`*.gba`) ist **nicht** Teil dieses Repositories
- Alle Offsets beziehen sich auf die **deutsche Version (Game Code: BPRD)**
