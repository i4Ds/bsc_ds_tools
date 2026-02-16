# Git

> [!NOTE]
> **Git** ist ein Versionsverwaltungssystem. **GitHub/GitLab** sind Plattformen, auf denen Git-Repositories online gespeichert und geteilt werden können.
>
> Falls du VS Code noch nicht installiert hast, folge zuerst der Anleitung in `install_python.md` (Abschnitt „Installation der IDE“).

## Git installieren

### Windows (Chocolatey)

Installiere Chocolatey, falls du das nicht bereits getan hast: [install_choco_windows](install_choco_windows.md).

Installiere nun git mit Chocolatey:

```powershell
choco install git -y
```

### macOS (Homebrew)

Installiere Homebrew, falls du das nicht bereits getan hast: [install_homebrew_macos](install_homebrew_macos.md).

Installiere nun git mit Homebrew:

```sh
brew install git
brew install --cask git-credential-manager
```

## Installation testen

Öffne ein Terminal (z. B. PowerShell oder CMD) und prüfe:

```sh
git --version
```

Wenn eine Versionsnummer angezeigt wird, ist Git korrekt installiert.
