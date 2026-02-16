## Chocolatey (Windows)

> [!NOTE]
> Chocolatey ist ein Paketmanager für Windows – ähnlich wie Homebrew auf macOS. Damit kannst du Software komfortabel über die Kommandozeile installieren und aktualisieren.
>
> In diesen Schritten nutzt du Chocolatey, um später Python (über `uv`) einfach zu installieren und aktuell zu halten.

## Chocolatey installieren

1. Öffne **PowerShell als Administrator**  
   - Im Startmenü nach „PowerShell" suchen  
   - Rechtsklick → **Als Administrator ausführen**

2. (Optional) Falls deine Execution Policy sehr streng ist, kannst du sie für diese Sitzung lockern:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force
```

3. Führe nun den offiziellen Installationsbefehl von Chocolatey aus (in der **Administrator‑PowerShell**):

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; `
[System.Net.ServicePointManager]::SecurityProtocol = `
[System.Net.ServicePointManager]::SecurityProtocol -bor 3072; `
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Warte, bis die Installation abgeschlossen ist. Anschliessend kannst du prüfen, ob Chocolatey funktioniert:

```powershell
choco --version
```

Dabei sollte dir eine Versionsnummer angezeigt werden.

## Mit Chocolatey installierte Programme aktualisieren

Um alle über Chocolatey installierten Pakete auf den neuesten Stand zu bringen, kannst du in einer **PowerShell als Administrator** folgenden Befehl ausführen:

```powershell
choco upgrade all -y
```

- `upgrade all`: aktualisiert alle installierten Pakete  
- `-y`: bestätigt alle Rückfragen automatisch

## Chocolatey‑Pakete automatisch aktualisieren (optional, empfohlen)

Statt manuell `choco upgrade all -y` auszuführen, kannst du direkt in der bereits geöffneten Admin‑PowerShell eine geplante Aufgabe einrichten, die das täglich für dich erledigt:

```powershell
$daily = New-ScheduledTaskTrigger -Daily -At 3:00AM
$startup = New-ScheduledTaskTrigger -AtStartup
$action = New-ScheduledTaskAction -Execute "choco.exe" -Argument "upgrade all -y"
$settings = New-ScheduledTaskSettingsSet -AllowStartIfOnBatteries -StartWhenAvailable
Register-ScheduledTask -TaskName "Choco Upgrade" -Trigger $daily,$startup -Action $action -Settings $settings -RunLevel Highest -User SYSTEM
```

- **Täglich um 03:00** und **bei jedem Hochfahren** wird `choco upgrade all -y` ausgeführt.
- `-StartWhenAvailable`: Falls der PC um 03:00 im Schlafmodus war, wird das Update nachgeholt, sobald er wieder aktiv ist.
- `-AllowStartIfOnBatteries`: Funktioniert auch im Akkubetrieb (Laptop).
- Du kannst die Uhrzeit bei `-At` anpassen.

## uv mit Chocolatey installieren

`uv` ist ein sehr schneller Paket‑ und Projektmanager für Python. Unter Windows kannst du `uv` direkt mit Chocolatey installieren:

```powershell
choco install uv -y
```

Danach kannst du testen, ob `uv` korrekt installiert ist:

```powershell
uv --version
```

## Python mit uv installieren

`uv` kann Python‑Versionen für dich installieren und verwalten. Damit du Python wie gewohnt mit `python myscript.py` verwenden kannst, installierst du eine Version als Standard‑Python. Der folgende Befehl installiert z. B. Python 3.13, registriert sie als Standard und sorgt dafür, dass `python` im `PATH` verfügbar ist:

```powershell
uv python install --default 3.13
```

- `--default`: richtet `python` / `python3`‑Aufrufe auf diese Version aus  

Wenn der Befehl erfolgreich war, kannst du die Installation testen:

```powershell
python --version
```

Es sollte eine Python‑3.13‑Version angezeigt werden.

### Python‑Skripte ausführen

Nach der Installation kannst du Python‑Dateien wie gewohnt ausführen. Wechsle in ein Verzeichnis mit deinem Skript und führe z. B. aus:

```powershell
python my_script.py
```

### Python interaktiv ausprobieren

Du kannst auch die interaktive Python‑Konsole starten:

```powershell
python
```

Gib dort z. B. `10*10` ein und bestätige mit Enter.  
Beenden kannst du die Konsole mit:

```python
exit()
```

oder mit `Strg+Z` gefolgt von Enter (unter Windows).
