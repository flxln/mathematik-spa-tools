# SCORM-Paket: Kongruenz-Trainer

SCORM-1.2-Inhalt für Moodle (`mod_scorm`). Eine Sitzung besteht aus **8 Runden** (Schätzung kongruent ja/nein, dann Auswerten).

## Paket bauen

Im Ordner `scorm/kongruenz_trainer/` alle Dateien **mit `imsmanifest.xml` im ZIP-Root** packen:

```bash
cd scorm/kongruenz_trainer && zip -r ../../kongruenz_trainer_scorm12.zip imsmanifest.xml kongruenz_trainer.html assets/
```

Das Archiv liegt danach im Projektroot als `kongruenz_trainer_scorm12.zip` (wird bei Bedarf mit dem Befehl überschrieben).

In Moodle: Kurs → **Aktivität anlegen** → **SCORM-Lernpaket** → ZIP hochladen.

## Bewertung und Berichte

- **`cmi.core.score.raw`**: Anzahl richtiger Schätzungen (0–8).  
- **`cmi.core.score.max`**: 8.  
- **`cmi.core.lesson_status`**: nach Abschluss aller Runden `completed`.  
- **`cmi.interactions.0` … `7`**: je Runde `true-false`, Ergebnis `correct` / `wrong`, Antwort und Muster als `t`/`f` (kongruent ja/nein).

In der SCORM-Aktivität unter **Bewertung** die Methode so wählen, dass die **Rohpunktzahl** (`cmi.core.score.raw`) ins Notenbuch übernommen wird (nicht nur „Abschluss“, sofern du eine Note brauchst).

**Versuche:** Mehrfaches Durchspielen zählt Moodle pro **SCORM-Versuch** (Aktivitätseinstellung „Anzahl der erlaubten Versuche“). Ein erneutes „Nochmal spielen“ **nach** abgeschlossener Sitzung aktualisiert die SCORM-Werte in derselben LMS-Sitzung nicht erneut (API ist bereits beendet); für eine neue Bewertung ist ein neuer Moodle-Versuch nötig.

## Lokaler Test

Ohne LMS meldet die Seite nichts an SCORM; der Trainer funktioniert normal im Browser.

## Quelle

Die Spiel-Logik entspricht [`kongruenz_trainer.html`](../../kongruenz_trainer.html) im übergeordneten Projekt; diese Kopie enthält die SCORM-Laufzeit und keine Übersichts-Navigation.
