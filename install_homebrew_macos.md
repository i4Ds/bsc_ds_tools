# Homebrew (macOS)

> [!NOTE]
> Homebrew ist ein Paketmanager für macOS. Er erleichtert die Installation und Verwaltung von Software, die nicht standardmässig auf macOS enthalten ist.
>
> Es lohnt sich, Python über `uv` zu installieren, da es den Installationsprozess vereinfacht. `uv` installieren wir mittels Homebrew. Läuft mal was schief, kannst du Python schnell neu installieren. Auch die Installation anderer Python Versionen kann mit nur einem Befehl erledigt werden. Im Module [GPR](https://spaces.informatik.fhnw.ch/spaces/grundkompetenz-programmieren) werdet ihr `uv` näher kennenlernen.

## Homebrew Installation

Um Homebrew zu installieren, öffne den Terminal und kopier diesen Befehl hinein:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Drücke auf Enter, gib dein Administratorpasswort ein und bestätige die Installation.

Nach der Installation fordert Homebrew dich auf, die PATH-Variable zu setzen:
![](https://i.imgur.com/wgPvh5p.png)

Kopiere den Befehl, den Homebrew dir anzeigt (er könnte anders als bei mir sein), und füge ihn in dein Terminal ein. Drücke Enter, um die PATH-Variable zu setzen.

Brew ist nun installiert und einsatzbereit. Du kannst das testen, indem du folgenden Befehl ausführst:

```sh
brew --version
```

Dabei sollte dir die Brew-Version angezeigt werden.

## Mit Brew installierte Programme aktualisieren

Um alle über Homebrew installierten Programme auf den neuesten Stand zu bringen:

```sh
brew update
brew upgrade
```

`brew update` aktualisiert Homebrew selbst, `brew upgrade` aktualisiert alle installierten Formulae.

### Brew-Programme automatisch aktualisieren (optional, empfohlen)

Statt manuell `brew update` und `brew upgrade` auszuführen, kannst du Homebrew so einrichten, dass es sich automatisch im Hintergrund aktualisiert. Das sorgt dafür, dass deine installierten Programme immer auf dem neuesten Stand sind:

```sh
brew install pinentry-mac && brew tap homebrew/autoupdate && brew autoupdate start --upgrade --cleanup --immediate --sudo --ac-only
```

Dieser Befehl installiert `pinentry-mac` (für sichere Passwort-Eingabe), aktiviert das `autoupdate`-Plugin und startet automatische Updates mit Upgrade, Cleanup und sofortiger Ausführung.

## uv installieren

`uv` ist ein schneller Paket- und Projektmanager für Python (Versionen, Umgebungen, Abhängigkeiten). Du installierst es über Homebrew:

```sh
brew install uv
```

Nach der Installation kannst du die Version prüfen:

```sh
uv --version
```

## Python mit uv installieren

Eine Python-Version installierst du so (z. B. 3.13). Mit `--default` landet sie im PATH, dann funktioniert `python` überall:

```sh
uv python install --default 3.13
```

### Python-Dateien ausführen

Danach kannst du wie folgt Python-Dateien ausführen:

```sh
python my_script.py
```

In einem Projekt mit `pyproject.toml` nutzt du später `uv run python`, damit die richtige Version und Umgebung verwendet wird.

### Python interaktiv ausprobieren

Du kannst auch die Python-Konsole starten: `python` eingeben, dort z. B. `10*10` eingeben und mit der Entertaste bestätigen und mit `exit()` oder Strg+D wieder verlassen.
