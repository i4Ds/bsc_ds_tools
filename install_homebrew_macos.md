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