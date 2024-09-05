# Installation

## Windows
### Python 3.x Installation
### Einstellungen
### Packages

## macOS
### Homebrew Installation
Homebrew ist ein Paketmanager für macOS. Er erleichtert die Installation und Verwaltung von Software, die nicht standardmäßig auf macOS enthalten ist.Homebrew ist ein Paketmanager für macOS. Er erleichtert die Installation und Verwaltung von Software, die nicht standardmäßig auf macOS enthalten ist.

Es lohnt sich, Python über Homebrew zu installieren, da es alle komplizierten Einstellungen automatisch für dich erledigt. Läuft mal was schief, kannst du Python schnell neu installieren. Auch die Installation anderer Python Versionen kann mit nur einem Befehl erledigt werden.

Um Homebrew zu installieren, öffne den Terminal und kopier diesen Befehl hinein:
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Drücke auf Enter, gibt dein Administratorpasswort ein und bestätige die Installation. 

Nach der Installation fordert Homebrew dich auf, die PATH-Variable zu setzen:
![](https://i.imgur.com/wgPvh5p.png)

Kopiere den Befehl, den Homebrew dir anzeigt (er könnte anders als bei mir sein), und füge ihn in dein Terminal ein. Drücke Enter, um die PATH-Variable zu setzen.

Brew ist nun installiert und einsatzbereit. Du kannst das testen, indem du folgenden Befehl ausführst:
```sh
brew --version
```
Dabei sollte dir die Brew-Version angezeigt werden.

### Python 3.x Installation
Nutze Homebrew um eine beliebige Python Version zu installieren:

Der Terminal-Befehl dafür lautet wie folgt:
```sh
brew install python@<VERSION>
```

Um beispielsweise Python 3.12 zu installieren, müsste man folgenden Befehl ausführen
```sh
brew install python@3.12
```

![](https://i.imgur.com/w7OPLAx.gif)

#### Packages
Ein Package in Python ist eine Sammlung von Modulen, die bestimmte Funktionen und Werkzeuge enthalten. Ein Modul ist einfach eine Datei, die Python-Code enthält, und ein Package organisiert mehrere dieser Module in einer Struktur, die es einfacher macht, wiederverwendbare Codeblöcke zu verwalten.

Beispiel: Das "numpy"-Package enthält verschiedene Module, die mathematische Funktionen bereitstellen. Wenn du zum Beispiel mit großen Zahlen oder Matrizen arbeiten möchtest, kannst du mit numpy bereits fertige Werkzeuge nutzen, anstatt diese selbst programmieren zu müssen.

Um neue Packages zu installieren, nutze pip. Pip ist ein Paketmanager für Python, der es dir ermöglicht, Packages aus dem Python Package Index (PyPI) zu installieren und zu verwalten.

Um ein Package zu installieren, öffne den Terminal und führe folgenden Befehl aus:
```sh
pip3.12 install <PACKAGE1> <PACKAGE2> <PACKAGE3> ...
```

Beispiel: Um das jupyter- und numpy-Package zu installieren, führe folgende Befehle aus:
```sh
pip3.12 install jupyter numpy 
```

Es könnte sein, dass bei neueren Python-Versionen diese Befehle zu einem Fehler führen. Probiere in diesem Fall dies aus:
```sh
pip3.12 install jupyter numpy --break-system-packages
```

# Aufsetzen der IDE

# Erste Codezeilen