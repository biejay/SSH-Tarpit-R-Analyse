# SSH-Tarpit-R-Analyse
## Analyse der [SSH-Tarpit Logs](https://pypi.org/project/ssh-tarpit/) via R

### Features:
* Wer sind die Top #10 Angreifer
* IP-Geolocate: Woher kommen die Angreifer?
* Wie lange bleiben die Angreifer in deiner Tarpit kleben?
* Aus welchen Subnetzen stammen die Angreifer?
* interaktives Netzwerk-Diagramm von Subnetzen und IPs
* interaktive Weltkarte mit Angreifern
* Wann wirst du angegriffen?
* und mehr!

### Beispiele:
<img src="https://user-images.githubusercontent.com/8942784/120938542-871c0a80-c713-11eb-8f6f-bb7eb06cfa15.JPG" width="800" height="400" alt="topten">
<img src="https://user-images.githubusercontent.com/8942784/120938551-8edbaf00-c713-11eb-8e8a-e0b21c6bea65.JPG" width="800" height="400" alt="klebezeiten">
<img src="https://user-images.githubusercontent.com/8942784/120938552-900cdc00-c713-11eb-9d60-867248b15c6e.JPG" width="700" height="600" alt="netzwerk-diagramm">
<img src="https://user-images.githubusercontent.com/8942784/120938571-a4e96f80-c713-11eb-8ccc-21799de33972.JPG" width="800" height="600" alt="Weltkarte">


### How-To:
* die tarpit-logs (*tarpit.txt*) werden als CSV benötigt! Dafür am besten mit diesem Python-Skript die .txt Datei in eine .csv umwandeln: [github/tarpit_log_to_csv](https://github.com/biejay/tarpit_log_to_csv)
* [R-Studio](https://www.rstudio.com/products/rstudio/) installieren
* [tarpit_auswertung.rmd](https://raw.githubusercontent.com/biejay/SSH-Tarpit-R-Analyse/main/tarpit_auswertung.Rmd) runterladen und in selbes Verzeichnes wie *tarpit.csv* legen
* Weltkarte runterladen und entpacken: http://thematicmapping.org/downloads/TM_WORLD_BORDERS_SIMPL-0.3.zip 
    * *TM_WORLD_BORDERS_SIMPL-0.3.shp* und die anderen Dateien müssen im selben Verzeichnis liegen wie das .rmd und das .csv File! 
* *tarpit_auswertung.rmd* mit Rstudio öffnen 
* *Session* -> *Set Working Directory* -> *To Source File Location*
* das Laden zusätzlicher Pakete ist nötig, wenn diese noch nicht installiert sind. Einfach: `install.packages("HIER_PAKETNAME")`
* ein HTML-Markdown erzeugen - Fertig
