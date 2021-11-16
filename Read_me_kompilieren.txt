Wichtig:
Um Fehler und Probleme beim Kompilieren zu vermeiden, benutzen Sie bitte immer die aktuelle Version Ihres Betriebssystems (Windows / Mac / Linux), die aktuelle Version Ihrer LaTeX-Distribution (MiKTeX / MacTeX / Tex Live) und die aktuelle Version Ihres Setzprogramms beziehungsweise LaTeX-Editors (TeXstudio / Texmaker / TeXworks / TeXnicCenter). Aktualisieren Sie Ihr Betriebssystem, Ihre LaTeX-Distribution und Ihren LaTeX-Editor vor dem Kompilieren dieser Vorlage oder lassen Sie diese von Ihrem IT-Beauftragten der Abteilung aktualisieren.




Hinweise zum Kompilieren / Setzreihenfolge:
Für die korrekte Darstellung des Layouts sowie der Bibliografien (multibib) kompilieren Sie bitte wie folgt (siehe Reihenfolge der Kompiliervorgänge):

- Windows 10: über die Eingabeaufforderung PowerShell bzw. Eingabeaufforderung (cmd).
Gehen Sie dazu in den Ordner dieses Projekts, wählen Sie keine Datei an, klicken Sie auf eine leere Stelle mit der linken Maustaste und öffnen Sie das Kontextmenü bei gedrückter Umschalttaste (Umschalttaste + rechter Mausklick) und wählen Sie "PowerShell-Fenster hier öffnen". Geben Sie anschließend "cmd" ein und rufen Sie die Kompiliervorgänge einzeln wie folgt auf (siehe Reihenfolge der Kompiliervorgänge):

- macOS Big Sur: über das Terminal.
Gehen Sie dazu in den Überordner dieses Projekts und wählen den Ordner an, in dem sich das Projekt befindet. Öffnen Sie nun das Kontextmenü (Sekundärklick) durch Drücken von Control+Maustaste oder beim Trackpad durch ein kurzes Tippen/Klicken mit zwei Fingern. Wählen Sie nun (Dienste)/„Neues Terminal beim Ordner“ und rufen Sie die Kompiliervorgänge einzeln wie folgt auf:




Reihenfolge der Kompiliervorgänge:
 pdflatex KSP_Diss_A5
 bibtex KSP_Diss_A5
 bibtex journal					% Der Dateiname der mit Bibtex auszuführenden Datei wird im Befehl "\newcites{journal}" in dieser TeX-Datei angegeben
 bibtex conference				% Der Dateiname der mit Bibtex auszuführenden Datei wird im Befehl "\newcites{conference}" in dieser TeX-Datei angegeben
 pdflatex KSP_Diss_A5
 pdflatex KSP_Diss_A5




Anmerkungen zu TeXstudio:
In TeXstudio die Kompilieraufrufe dauerhaft ändern (Windows 10, TeXstudio 3.0.1):
Optionen/TeXstudio konfigurieren.../Erzeugen/ -> Und hier die Einträge unter "Standardcompiler" und "Standard Bibliographieprogramm" anpassen.

In TeXstudio die Kompilieraufrufe manuell ausführen (Windows 10, TeXstudio 3.0.1):
Tools/Befehle/ -> Und hier die Einträge "PDFLaTeX" und "Bibtex" (Bibtex kann jedoch nicht für bestimmte Dateien in TeXstudio ausgeführt werden, hierzu muss die Eingabeaufforderung genutzt werden s.o.).




Literaturverzeichnis, Zitierstil, Bibliografiestil:
Bitte beachten Sie, dass der Bibliografie- und Zitierstil in dieser Vorlage voraussichtlich nicht den Anforderungen Ihres Instituts entsprechen. Aufgrund der Vielfalt verschiedener Stile kann diese LaTeX-Vorlage einen exakt definierten Bibliografie- und Zitierstil für einzelne Anfragen nicht leisten. Bitte verwenden Sie die von Ihrem Institut bereitgestellten LaTeX-Pakete für die von Ihnen genutzten Stile und passen Sie den Bibliografiestil „\bibliographystyle{plainnat}“ in der Datei „Inhalt/Literaturverzeichnis.tex“ als auch den Zitierstil „\usepackage{natbib}“ in der Datei „KSP_Diss_A5.tex“ entsprechend Ihrem Bedarf an.  

Wenn Sie nicht alle Titel aus Ihrer Datei mit den bibliografischen Angaben (z. B. „Externe_Literatur.bib“) automatisch in das Literaturverzeichnis ausgeben möchten, entfernen Sie bitte die Befehle „\nocite{*}“ bzw. auch „\nocitejournal{*}“ und „\nociteconference{*}“ aus der Datei „Inhalt/Literaturverzeichnis.tex“.

Der Zähler für die Titel in den Literaturverzeichnissen (z. B. „Journalartikel“ oder „Konferenzbeiträge“) wird standardmäßig auf „[1]“ zurückgesetzt durch den optionalen Parameter „resetlabels“ für den Befehl „\usepackage[resetlabels]{multibib}“ in der Datei „KSP_Diss_A5.tex“. Wenn Sie eine fortlaufende Nummerierung der Titel für die Literaturverzeichnisse wünschen, entfernen Sie bitte den optionalen Parameter „resetlabels“ im oben genannten Befehl.
