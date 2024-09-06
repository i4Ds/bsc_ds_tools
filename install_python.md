# Python Vorbereitung

## Installation auf Windows
<details>
<summary>Python 3.12 Installation</summary><br>

Lade die neueste Version von Python 3.x vom Microsoft Store herunter:
- [Python 3.12](https://www.microsoft.com/store/productId/9NCVDN91XZQP)
 
Versionen von Python unter 3.10 sollten grundsätzlich nicht mehr verwendet werden.
</details><br>

## Installation auf macOS
<details>
<summary>Homebrew Installation</summary><br>
Homebrew nutzen wir, um Python (und R) zu installieren. 

Was das ist und wie man es installiert, wird hier erklärt:
- [Homebrew Installation auf macOS](install_homebrew_macos.md)
</details><br>

<details>
<summary>Python 3.12 Installation</summary><br>
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
</details><br>

## Packages
Ein Package in Python ist eine Sammlung von Modulen, die bestimmte Funktionen und Werkzeuge enthalten. Ein Modul ist einfach eine Datei, die Python-Code enthält, und ein Package organisiert mehrere dieser Module in einer Struktur, die es einfacher macht, wiederverwendbare Codeblöcke zu verwalten.

Beispiel: Das "numpy"-Package enthält verschiedene Module, die mathematische Funktionen bereitstellen. Wenn du zum Beispiel mit großen Zahlen oder Matrizen arbeiten möchtest, kannst du mit numpy bereits fertige Werkzeuge nutzen, anstatt diese selbst programmieren zu müssen.

Um neue Packages zu installieren, nutze pip. Pip ist ein Paketmanager für Python, der es dir ermöglicht, Packages aus dem Python Package Index (PyPI) zu installieren und zu verwalten.

Um ein Package zu installieren, öffne den Terminal (auf Windows die Eingabeaufforderung) und führe folgenden Befehl aus:
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

## Aufsetzen der IDE

## Erste Codezeilen