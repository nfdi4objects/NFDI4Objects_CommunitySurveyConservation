# Daten zur Community Umfrage

Dieser Ordner enthält die **offenen Daten** der Community-Umfrage in verschiedenen Formen.  
Allgemeine Informationen zur Umfrage, Mitwirkung und Zielsetzung finden sich in der README auf der obersten Projektebene.

---

## Verzeichnis & Inhalte

-**`questionnaire.md`**

Enthält den vollständigen Fragenkatalog der Umfrage in Markdown-Form sowie die Verlinkung zu der im Vorfeld der Umfrage veröffentlichten Version.

-**`raw_responses.csv`**  

  Tabelle mit den **anonymisierten Einzelantworten** in CSV-Format
  - Zeile = Antworten einer teilnehmende Person
  - Spalten = Frage + Antwortenoption
  - Freitextantworten und Kommentare wurden im Sinne der Anonymisierung entfernt (→ siehe Abschnitt *Anonymisierung*).

-**`frequency_analysis.csv`**

  Tabelle mit der **statistischen Auswertung** (Häufigkeiten/Prozentwerte) pro Frage  
  - Zeile = Jeweilige Antwortenoption
  - Spalte = Kontext, Häufigkeitsverteilung und methodische Zusatzinformationen  
    #### Spaltenbeschreibung:  
      | Spalte | Beschreibung |
      |--------|-------------|
      | `question_id` | Eindeutige Kennung der Frage|
      | `topic_block` | Kategorisierung nach Themenbereichen |
      | `question_text` | Vollständiger Fragewortlaut |
      | `answer_id` | Eindeutige Kennung der Antwortoption
      | `answer_text` | Wortlaut der Antwortoption (inkl. [Keine Antwort]) |
      | `answer_source` | Angabe, ob Antwortoption vorgegeben oder aus Kommentaren aggregiert |
      | `answer_count` | Absolute Häufigkeit dieser Antwortoption |
      | `count_valid`| Anzahl der gültigen Antworten für diese Frage (= Gesamtanzahl minus [keine Antwort] |
      | `percent_total` | Prozent bezogen auf alle Teilnehmenden |
      | `percent_valid` | Prozent bezogen auf gpltige Antworten dieser Frage
      | `condition` | Filterbedingung, falls Frage nur eingegrenzter Teilgruppe angezeigt wurde |
  
    #### Besonderheiten
    - **[keine Antwort]:** Sind nicht einfach technische "missing values", sondern inhaltlich relevante Nicht-Antworten der Teilnehmenden und wurden daher als eigene Antwortenoption in die statistische Auswertung aufgenommen.
    - **Bedingte Fragen:** Einige Fragen 
