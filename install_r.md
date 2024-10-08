# R und RStudio

R und RStudio sind kostenlose, quelloffene Werkzeuge, die für statistische Berechnungen und Datenvisualisierung verwendet werden. R ist die Programmiersprache und RStudio ist das Werkzeug, um R-Code zu schreiben und auszuführen. R wird im Modul [Explorative Datenanalyse (EDA)](https://spaces.technik.fhnw.ch/spaces/explorative-datenanalyse) verwendet, in dem die Studierenden lernen, wie man Daten mit R einliest, bereinigt, visualisiert und analysiert. [Programmieren in R (PRR)](https://spaces.technik.fhnw.ch/spaces/programmieren-in-r) bietet einen tiefergehenden Einblick in das Programmieren mit R.

## Auf Windows installieren

Dieser R-Bloggers-Blogpost [Tutorial: Getting Started with R and RStudio](https://www.r-bloggers.com/2020/08/tutorial-getting-started-with-r-and-rstudio/) bietet eine Schritt-für-Schritt-Anleitung zur Installation von R und RStudio auf Windows. Er bietet auch einen Anleitung für die Installation unter macOS, aber für macOS gibt es hier eine spezifischere Anleitung im nächsten Abschnitt.

### Installieren für fortgeschrittene Benutzer

Für all die ohne Anleitung auskommen, RStudio und R könne hier heruntergeladen werden: [RStudio Download](https://www.r-bloggers.com/2020/08/tutorial-getting-started-with-r-and-rstudio/).

## Auf macOS installieren

1. Um R auf macOS zu installieren, nutzen wir Homebrew. Was das ist und wie man es installiert, wird hier erklärt: [Homebrew Installation auf macOS](install_homebrew_macos.md)

2. Um R zu installieren, führe folgenden Befehl im Terminal aus:

    ``` zsh
    brew install --cask r
    ```

3. Um RStudio zu installieren, führe folgenden Befehl im Terminal aus:

    ``` zsh
    brew install --cask rstudio
    ```

## RStudio kennenlernen

RStudio ist in vier Bereiche unterteilt:

Bild:

![RStudio](https://docs.posit.co/ide/user/ide/guide/ui/images/rstudio-panes-labeled.jpeg)

1. **Source**: Hier schreibst du deinen R-Code.
2. **Console**: Hier siehst du die Ausgabe deines Codes.
3. **Environments**: Hier siehst du die Variablen, die du im Code definiert hast.
4. **Output**: Hier siehst du die Visualisierungen und Tabellen, die du im Code erstellt hast.

Mehr dazu findest du in der [RStudio-Dokumentation](https://docs.posit.co/ide/user/ide/guide/ui/ui-panes.html).

### Umgebung speichern

Es ist möglich die Umgebung (Variablen, Funktionen, etc.) in RStudio zu speichern. Dies wird für den Anfang nicht empfohlen da es zu Verwirrung führen kann. Daher wird diese Option abgeschaltet:

1. Gehe zu `Tools` > `Global Options` > `General`. Unter dem Punkt `Workspace` setze den Punkt `Save workspace to .RData on exit` auf `Never`.

## Packages

Packages erweitern die Funktionalität von R. Es gibt tausende von Packages, die für verschiedene Anwendungen entwickelt wurden. Packages können über den Tab `Packages` installiert werden. Alternativ können Packages in der RStudio-Console mit dem Befehl `install.packages("package_name")` installiert werden. Das Package `tidyverse` sollte bei jeder R-Installation dazu installiert werden.

Um zu überprüfen, ob `tidyverse` installitert ist, kann z. B. folgender Code ausgeführt werden:

``` r
library(ggplot2)
mpg_plot <- ggplot(mpg, aes(x=displ, y = hwy)) +
  geom_point(aes(colour = class))

mpg_plot
```

## Einführung in R

W3Schools bietet eine [Einführung in R](https://www.w3schools.com/r/) an. Diese ist für Studis im ersten Semester sehr hilfreich, um die Grundlagen von R zu lernen.
