### Luka Maric | Leon Marazovic

## Git Merging Aufgabe

---

## 1) Schritt 1: Initiales Setup

Dieser Abschnitt behandelt die **Erstellung des Repositorys** und den ersten Commit.

Repository auf GitHub erstellen
Lokal: git init
Verbinden: git remote add origin "repo"
Datei erstellen: echo "" >> onMain.md
Staging: git add onMain.md
Commit: git commit -m "message"
Push: git push

---

## 2) Schritt 2: Feature-Branch erstellen und Pushen

Hier wird der neue Branch (`a-feature`) erstellt und zum ersten Mal hochgeladen.

Neuen Branch erstellen: git branch a-feature
Branch wechseln: git checkout a-feature
Branch initial pushen:
git add .
git commit -m "initial commit"
git push --set-upstream origin a-feature
Neue Datei erstellen: echo "" >> onBranch.md
Hinzufügen, committen, pushen:
git add onBranch.md
git commit -m "added file onBranch.md"
git push

---

## 3) Schritt 3: Änderungen auf dem Feature-Branch

Die Arbeit wird auf dem Feature-Branch fortgesetzt.

Branch wechseln: git checkout a-feature
Datei bearbeiten und committen:
git add onBranch.md
git commit -m "message"
History prüfen: git log

---

## 4) Schritt 4–6: Git-History prüfen

Dieser Abschnitt dient der Überprüfung der Historie, bevor Branches zusammengeführt werden.

Git-History prüfen: violetter Strich = main, anderer = a-feature
Detaillierte Historie: git log
Unterschiedliche Inhalte, da Commits nicht automatisch auf anderen Branches erscheinen

---

## 5) Schritt 7–9: Änderungen auf dem Main-Branch

Parallel zur Arbeit am Feature-Branch werden Änderungen am `main`-Branch vorgenommen.

Zeilen in onMain.md hinzufügen
Änderungen:
git add onMain.md
git commit -m "added lines"
History prüfen: git log

---

## 6) Schritt 10–12: Feature-Branch aktualisieren

Der Feature-Branch (`a-feature`) wird mit den neuesten Änderungen vom `main`-Branch synchronisiert (gemergt).

Auf Feature-Branch wechseln: git checkout a-feature
Main-Branch mergen: git merge maina
