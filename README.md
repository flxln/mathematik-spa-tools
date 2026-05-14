# Mathematik-SPA-Tools

Sammlung statischer, einseitiger Web-Übungen (HTML/CSS/JavaScript) für den Mathematikunterricht. Kein Build-Schritt; geeignet für **GitHub Pages** und Verlinkung aus **Moodle**.

## Inhalt

| Seite | Beschreibung |
|--------|----------------|
| [index.html](index.html) | Übersicht aller Tools |
| [bruch_kopfrechnen_trainer.html](bruch_kopfrechnen_trainer.html) | Kopfrechnen Bruchrechnung |
| [gemischte_aufgaben_trainer.html](gemischte_aufgaben_trainer.html) | Gemischte Rechenaufgaben |
| [malfolgen_trainer.html](malfolgen_trainer.html) | Malfolgen |
| [winkel_gerade_kreuzungen_progression.html](winkel_gerade_kreuzungen_progression.html) | Winkel an geraden Kreuzungen (Progression) |

## Lokal testen

- Datei `index.html` im Browser öffnen, oder
- im Projektordner: `npx --yes serve .` und die angezeigte lokale URL nutzen (Pfade zu `assets/` funktionieren dann wie auf Pages).

## GitHub Pages

1. Repository auf GitHub anlegen und diesen Ordner als Inhalt pushen (Branch `main`).
2. Unter *Settings → Pages*: Quelle **Deploy from branch**, Branch **main**, Ordner **/ (root)**.
3. Öffentliche Basis-URL hat die Form: `https://<benutzername>.github.io/<repository>/`  
   Einzel-Tools: z. B. `…/bruch_kopfrechnen_trainer.html`.

## Moodle

- **URL-Ressource:** Link zur gewünschten `https://…`-Adresse; oft stabiler, die Aktivität in einem **neuen Fenster** öffnen zu lassen.
- **Iframe:** möglich über „Seite“ oder Einbettungs-Plugins; ggf. muss die Pages-URL in den Moodle-Sicherheitseinstellungen als **vertrauenswürdige URL** eingetragen sein. Auf Darstellung im iframe prüfen (Höhe, Scrollen).

## Lizenz

Dieses Projekt steht unter der **MIT License**, siehe [LICENSE](LICENSE).

Beiträge (Verbesserungen, neue Tools, Fehlerkorrekturen) sind willkommen; am besten per Pull Request oder Issue im GitHub-Repository.
