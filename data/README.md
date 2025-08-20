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
      | `percent_valid` | Prozent bezogen auf gültige Antworten dieser Frage
      | `condition` | Filterbedingung, falls Frage nur eingegrenzter Teilgruppe angezeigt wurde |
  
    #### Besonderheiten
    - **[keine Antwort]:**  
      Sind nicht einfach technische "missing values", sondern inhaltlich relevante Nicht-Antworten der Teilnehmenden und wurden daher als eigene Antwortenoption in die statistische Auswertung aufgenommen.
    - **Bedingte Fragen:**  
      Einige Fragen wurden nur einer eingegrenzten Teilgruppe angezeigt, basierend auf deren Antworten vorheriger Fragen. Diese Sprunglogiken sind durch die `condition`-Spalte gekennzeichnet.
      Bei diesen Fragen bezieht sich die Prozentangabe in der Spalte `percent_total` **nicht** auf die Gesamtteilnehmerzahl der Umfrage, sondern lediglich auf die Teilnehmerzahl, denen diese Frage überhaupt angezeigt wurde. 
    - **Prozentangaben:**  
      Für die Spalte `percent_total` wurde als Basis für die Berechnung, außer bei den bedingten Fragen, die bereinigte Gesamtteilnehmerzahl von 240 Personen  verwendet.
      Die Spalte `percent_valid` bezieht sich auf die Anzahl an Teilnehmenden, die bei der jeweiligen Frage mindestens eine Antwortoption ausgewählt haben (= `count_valid`).
   - **Korrelationen**  
     Bei dieser Tabelle ist lediglich eine einfache Häufigkeitsauswertung enthalten. Korrelationen zwischen mehreren Fragen/Antwort-Kombiantionen werden ggf. zu einem späteren Zeitpunkt separat bereitgestellt.

---

## Anonymisierung und Datenschutz  
Teilnehmende der Umfrage hatten die Möglichkeit am Ende der Umfrage für Detailfragen und weiterführende Interviews freiwillig ihre Kontaktdaten zu hinterlassen. Diese Daten sind aus datenschutzrechtlichen Gründen nur der Umfragenadministration zugänglich und wurden aus der `raw_responses`-Datei entfernt. 
Darüber hinaus werden Freitextantworten, Kommentare sowie eine Abschlussfrage zur Erwartungshaltung an NFDI4Objects **nicht veröffentlicht**, um Rückschlüsse auf Einzelpersonen zu verhindern. Diese Ergebnisse wurden in aggregierter Form in der schriftlichen Auswertung (Whitepaper) dokumentiert.

      
