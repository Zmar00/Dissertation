Hinweise zum Kompilieren / Setzreihenfolge:

Für die korrekte Darstellung des Layouts sowie der Bibliografien (multibib) kompilieren Sie bitte wie folgt:

- Windows 10: über die Eingabeaufforderung PowerShell bzw. Eingabeaufforderung (cmd).
Gehen Sie dazu in den Ordner dieses Projekts, wählen Sie keine Datei an, klicken Sie auf eine leere Stelle mit der linken Maustaste und öffnen Sie das Kontextmenü bei gedrückter Umschalttaste (Umschalttaste + rechter Mausklick) und wählen Sie "PowerShell-Fenster hier öffnen". Geben Sie anschließend "cmd" ein und rufen Sie die Kompiliervorgänge einzeln wie folgt auf:

- macOS Big Sur 11.0.1: über das Terminal.
Gehen Sie dazu in den Überordner dieses Projekts und wählen den Ordner an, in dem sich das Projekt befindet. Öffnen Sie nun das Kontextmenü (Sekundärklick) durch Drücken von Control+Maustaste oder beim Trackpad durch ein kurzes Tippen/Klicken mit zwei Fingern. Wählen Sie nun (Dienste)/„Neues Terminal beim Ordner“ und rufen Sie die Kompiliervorgänge einzeln wie folgt auf:


- Reihenfolge der Kompiliervorgänge 
 pdflatex KSP_Diss_A5
 bibtex KSP_Diss_A5
 bibtex journal					% Der Dateiname der mit Bibtex auszuführenden Datei wird im Befehl "\newcites{}" in dieser TeX-Datei angegeben
 bibtex conference				% Der Dateiname der mit Bibtex auszuführenden Datei wird im Befehl "\newcites{}" in dieser TeX-Datei angegeben
 pdflatex KSP_Diss_A5
 pdflatex KSP_Diss_A5


Fertig.



Anmerkungen

In TeXstudio die Kompilieraufrufe dauerhaft ändern (Windows 10, TeXstudio 3.0.1):
Optionen/TeXstudio konfigurieren.../Erzeugen/ -> Und hier die Einträge unter "Standardcompiler" und "Standard Bibliographieprogramm" anpassen.

In TeXstudio die Kompilieraufrufe manuell ausführen (Windows 10, TeXstudio 3.0.1):
Tools/Befehle/ -> Und hier die Einträge "PDFLaTeX" und "Bibtex" (Bibtex kann jedoch nicht für bestimmte Dateien in TeXstudio ausgeführt werden, hierzu muss die Eingabeaufforderung genutzt werden s.o.).