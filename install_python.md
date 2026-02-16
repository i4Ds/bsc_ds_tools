# Python Vorbereitung

Python ist eine der beliebtesten Programmiersprachen der Welt. Sie wird in vielen Bereichen eingesetzt, darunter Webentwicklung, Datenanalyse, künstliche Intelligenz und vieles mehr. Python ist bekannt für seine einfache Syntax und seine Vielseitigkeit, was es zu einer grossartigen Sprache für Anfänger und Fortgeschrittene macht.

In diesem Guide zeigen wir dir, wie du Python auf deinem Computer installierst und einrichtest, um mit dem Programmieren zu beginnen.

## Python installieren

Wie du Python am besten Installiert, hängt vom Betriebsystem ab. Hier findest du die jeweilige Anleitung:
- [Windows](install_choco_windows.md)
- [macOS](install_homebrew_macos.md)

## Packages
> [!NOTE]
> Ein Package in Python ist eine Sammlung von Modulen, die bestimmte Funktionen und Werkzeuge enthalten. Ein Modul ist einfach eine Datei, die Python-Code enthält, und ein Package organisiert mehrere dieser Module in einer Struktur, die es einfacher macht, wiederverwendbare Codeblöcke zu verwalten.
>
> Beispiel: Das "numpy"-Package enthält verschiedene Module, die mathematische Funktionen bereitstellen. Wenn du zum Beispiel mit grossen Zahlen oder Matrizen arbeiten möchtest, kannst du mit numpy bereits fertige Werkzeuge nutzen, anstatt diese selbst programmieren zu müssen.

Um neue Packages zu installieren, nutze `uv`. UV ist ein Paketmanager für Python, der es dir ermöglicht, Packages aus dem Python Package Index (PyPI) zu installieren und zu verwalten.

Um ein Package zu installieren, öffne das Terminal (auf Windows heisst es "Eingabeaufforderung") im Projektordner und führe folgenden Befehl aus:
```sh
uv add <PACKAGE1> <PACKAGE2> <PACKAGE3>
```

Beispiel: Um das `jupyter`- und `numpy`-Package zu installieren:
```sh
uv add numpy jupyter
```

Falls im Ordner noch kein Python-Projekt existiert, initialisiere es zuerst mit folgendem Befehl:
```sh
uv init
```

Das erstellt ein `pyproject.toml`-File, in welchem die installierten Packages und deren Versionen gespeichert werden. So kannst du jederzeit nachvollziehen, welche Packages in deinem Projekt installiert sind.

## Installation der IDE
> [!NOTE]
> Eine **IDE** (Integrated Development Environment) ist eine Software, die Programmierer unterstützt, Code zu schreiben, zu testen und auszuführen. Sie bietet Werkzeuge wie einen Texteditor, Debugging-Tools und oft eine grafische Oberfläche, um Programme effizienter zu entwickeln.
> 
> **PyCharm** ist eine beliebte IDE speziell für Python-Programmierung. Es bietet viele nützliche Funktionen wie automatische Vervollständigung von Code, Fehlererkennung und einfache Integration von Paketen, um die Entwicklung mit Python zu erleichtern.

Für das Modul `gpr - Grundkompetenz Programmieren` wird empfohlen PyCharm zu verwenden (es ist natürlich auch erlaubt VS Code oder andere Editoren zu verwenden).  Für PyCharm könnt ihr unter folgendem Link eine Studentenlizenz für alle JetBrains IDEs (inklusive PyCharm) anfordern:
- [JetBrains - Free Educational Licenses](https://www.jetbrains.com/community/education/#students)

Danach könnt ihr über eures Konto oder über folgenden Link PyCharm herunterladen und installieren:
- [PyCharm Download](https://www.jetbrains.com/pycharm/)

oder über Homebrew (MacOS):
```sh
brew install --cask pycharm
```

Danach kann man die PyCharm IDE starten und sie mit dem JetBrains Account aktivieren.

![](https://i.imgur.com/qOy4Pu6.png)

Du bist jetzt bereit, Python-Code zu schreiben und auszuführen!

## Erste Codezeilen

Öffne PyCharm und erstelle ein neues Projekt. Dafür drücke auf den `New Project` Button.

![](https://i.imgur.com/jQmD7wn.png)

Danach kannst du den Projektnamen und den Speicherort auswählen. Übernehme den Projektnamen und die Einstellungen des untenstehenden Bildes und drücke auf `Create`.

![](https://i.imgur.com/kj7ATCk.png)

Jetzt hat PyCharm ein neues Projekt erstellt und die Entwicklungsumgebung geöffnet. Auf der linken Seite hat sich ein Reiter geöffnet, welcher alle Dateien im Projekt anzeigt.

Mach einen Rechtsklick auf das Projekt, drücke auf `Neu` und schlussendlich auf `Python File`. Jetzt öffnet sich ein Fenster mit einer Textbox und drei Optionen. Schreib in die Textbox `beispiel`, wähle die Option `Python file` und drücke Enter.

Jetzt hat PyCharm eine beispiel.py Datei erstellt, welche man im linken Reiter sehen kann. 

Gleichzeitig hat sich rechts ein neues Fenster geöffnet, in welchem man die neu erstellte Datei sehen und editieren kann.

Schreibe in die Datei folgenden Code:
```python
a = 10
b = 5

print("Die Variablen a + b addiert ergeben:")
print(a + b)
```

Drücke auf das grüne Play-Symbol, um den Code auszuführen. Die Ausgabe sollte folgendermassen aussehen:

![](https://i.imgur.com/r3YnJZW.png)

Glückwunsch! Du hast soeben deinen ersten Python-Code geschrieben und ausgeführt.

### Erklärung zum Code

> [!NOTE]
> Variablen sind Container für Daten. In diesem Fall haben wir zwei Variablen `a` und `b`, welche die Zahlen 5 und 10 haben. Mit `print()` können wir Text und Variablen auf der Konsole ausgeben. Um Text auszugeben, schreiben wir den Text in Anführungszeichen in die Klammern. 

> [!TIP]
> Gerne kannst du ausprobieren, was passiert, wenn du die Addition (+) durch eine Multiplikation (*), eine Division (/) oder eine Subtraktion (-) ersetzt.

## Tipps

> [!TIP]
> Floorcoaches sind jeden Dienstag und Donnerstag am von 10:00 bis 12:00 und von 14:00 bis 16:00 im 5.3 anwesend. Sind sind mit ihren neonfarbigen Westen nicht zu übersehen. Sie helfen dir bei Fragen zu Python, anderen Modulen und allem rund ums Studium. Nutze diese Ressource!

> [!IMPORTANT]
> Geht unbedingt in die `gpr - Grundkompetenz Programmieren` Kontaktstunden! Personen, welche regelmässig in die Sprechstunden gehen, haben eine DEUTLICH höhere Erfolgsrate. Je öfter, desto besser, jedoch muss es nicht jede Woche sein.
