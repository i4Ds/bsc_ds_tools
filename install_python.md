# Python Vorbereitung

Python ist eine der beliebtesten Programmiersprachen der Welt. Sie wird in vielen Bereichen eingesetzt, darunter Webentwicklung, Datenanalyse, künstliche Intelligenz und vieles mehr. Python ist bekannt für seine einfache Syntax und seine Vielseitigkeit, was es zu einer grossartigen Sprache für Anfänger und Fortgeschrittene macht.

In diesem Guide zeigen wir dir, wie du Python auf deinem Computer installierst und einrichtest, um mit dem Programmieren zu beginnen.

## Python installieren

Wie du Python am besten installierst, hängt vom Betriebssystem ab. Hier findest du die jeweilige Anleitung:

- [Windows](install_choco_windows.md)
- [macOS](install_homebrew_macos.md)

## Packages
>
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
>
> [!NOTE]
> Eine **IDE** (Integrated Development Environment) ist eine Software, die Programmierer unterstützt, Code zu schreiben, zu testen und auszuführen. Sie bietet Werkzeuge wie einen Texteditor, Debugging-Tools und oft eine grafische Oberfläche, um Programme effizienter zu entwickeln.
>
> **VS Code** ist ein schlanker Editor mit guten Python-Erweiterungen.

Für das Modul `gpr - Grundkompetenz Programmieren` wird empfohlen, VS Code zu verwenden.

macOS (Homebrew):

```sh
brew install --cask visual-studio-code
```

Windows (Chocolatey, PowerShell als Administrator):

```powershell
choco install vscode -y
```

Du bist jetzt bereit, Python-Code zu schreiben und auszuführen!

## Erste Codezeilen

Erstelle einen Ordner `python_project`. Diesen Ordner wirst du anschliessend mit VS Code öffnen:

Öffne VS Code und dann deinen Projektordner (`Datei` > `Ordner öffnen...`).

Erstelle im Explorer eine neue Datei mit dem Namen `example.py`.

Schreibe in die Datei folgenden Code:

```python
a = 10
b = 5

print("Die Variablen a + b addiert ergeben:")
print(a + b)
```

Öffne danach in VS Code ein Terminal (`Terminal` > `Neues Terminal`) und initialisiere das Projekt (das musst du nur einmal machen):

```sh
uv init
```

Führe danach aus:

```sh
uv run python beispiel.py
```

Wenn du `beispiel.py` anpasst, musst du den Befehl `uv run python beispiel.py` jedes Mal erneut ausführen, damit du den neuen Output siehst.

Glückwunsch! Du hast soeben deinen ersten Python-Code geschrieben und ausgeführt.

Mehr kurze Beispiele findest du in der [Python Kurzreferenz](python_kurzreferenz.md).

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
