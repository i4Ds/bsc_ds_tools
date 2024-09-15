# Git, GitHub, und GitHub Desktop

## Begriffe

- **GitHub**: ist wie Google Drive aber für Code. Es ist ein Ort, an dem Code gespeichert, geteilt, und bearbeitet werden kann.
- **Git**: GitHub verwendet Git im Hintergrund. Git macht die eigentliche Arbeit, GitHub ist die Webseite, die uns die Arbeit erleichtert.
- **GitHub Desktop**: ist ein Tool, mit dem wir Git und GitHub bedienen können.

## GitHub-Konto erstellen

Wichtig: verwendet eure private E-Mail-Adresse und nicht die E-Mail-Adresse der Hochschule, da das Konto sonst bei Verlassen der Hochschule verloren geht! Die Hochschul-E-Mail-Adresse kann später hinzugefügt werden.

Ein GitHub-Konto kann über folgenden Link erstellt werden: [github.com/signup](https://github.com/signup). Es sollte ein starkes Passwort gewählt werden um fremde Zugriffe zu verhindern.

## Installation

1. [Git](https://git-scm.com/download) herunterladen und installieren.
2. [GitHub Desktop](https://desktop.github.com/download/) herunterladen und installieren.

## GitHub Desktop einrichten

Nach der Installation von GitHub Desktop muss das Programm eingerichtet werden.

1. GitHub Desktop öffnen. Wenn GitHub Desktop zum ersten Mal geöffnet wird, erscheint die Willkommensseite:

    ![GitHub Desktop Welcome Page](images/github_desktop_welcome.png)

2. Auf `Sign in to GitHub.com` klicken und melde mit dem GitHub-Konto anmelden, das zuvor erstellt wurde.

   1. ![GitHub autorisieren](images/github_auth.png)
   2. Die Meldung, dass GitHub Desktop autorisiert werden soll, bestätigen.

        ![GitHub autorisieren](images/github_auth2.png)

   3. Die Meldung, dass zu GitHub Desktop gewechselt werden soll, bestätigen.

3. Falls gewünscht, kann der Name und die E-Mail-Adresse angepasst werden. Diese werden in gewissen Situationen öffentlich angezeigt:

    ![GitHub Desktop Git-Einstellungen](images/github_git_settings.png)

4. GitHub Desktop ist nun eingerichtet und bereit für die Verwendung:

    ![GitHub Desktop nach dem Installieren](images/github_done.png)

## Repository erstellen

Ein Repository ist ein Ordner, in dem Code gespeichert wird. Wird ein Ordner von Git verwaltet, so nennt man ihn ein Repository.

1. In GitHub Desktop auf `File` -> `New Repository` klicken.

    ![GitHub Desktop Repository erstellen](images/github_new_repo.png)
    ![GitHub Desktop neues Repository](images/github_new_repo2.png)

2. Repository auf GitHub "pushen" (hochladen):

    ![GitHub Desktop neues Repository](images/github_push.png)

3. Repository auf GitHub ansehen (`View on GitHub`):

    ![GitHub Desktop nach dem Pushen](images/github_push2.png)

4. Banknachbarn zum Repository einladen:

    1. ![GitHub Settings Collaborators Add People](images/github_collaborators.png)
    2. ![GitHub User suchen](images/github_search_user.png)

5. Einladung annehmen (E-Mail):

## Repository clonen

    1. Auf den grünen Button `Code` klicken und dann auf `Open with GitHub Desktop`:
        ![GitHub Repo Clonen](images/github_clone.png)
    2. Meldung dass GitHub Desktop geöffnet werden soll bestätigen:
    3. Ordner auswählen, in dem das Repository gespeichert werden soll:
        ![GitHub Repo Clonen](images/github_clone2.png)

## Änderungen machen und pushen (hochladen)

   1. Ordner mit Editor (z. B. RStudio, PyCharm, Visual Studio Code) öffnen.
   2. Dateien bearbeiten.
   3. In GitHub Desktop eine "auf `Commit to main` klicken:
        ![GitHub Desktop Commit](images/github_commit.png)
   4. Änderungen auf GitHub "pushen" in dem man auf `Push origin` klickt.

## Änderungen von anderen holen

   1. In GitHub Desktop auf `Fetch origin` klicken.
   2. In GitHub Desktop auf `Pull origin` klicken.

## Konflikte erzeugen und lösen (Optional, für Fotgeschrittene)

Sollten Konflikte oder andere Probleme mit Git auftreten, ist es am Anfang hilfreich, wenn man sich Hilfe bei den Floor Coaches, Dozenten oder anderen Studys holt.

   1. Zwei Personen bearbeiten die gleiche Datei.
   2. Person 1 pusht die Änderungen.
   3. Person 2 pusht die Änderungen.
   4. Person 2 erhält eine Fehlermeldung, dass die Änderungen nicht gepusht werden können.
   5. Person 2 holt die Änderungen von Person 1.
   6. Person 2 löst die Konflikte.
   7. Person 2 pusht die Änderungen.
