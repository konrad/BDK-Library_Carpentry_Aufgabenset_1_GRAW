# BDK-Library_Carpentry_Aufgabenset_1_GRAW

## 1. Text-Editor der Wahl

### Visual Studio Code

Für den Test der verschiedenen Text-Editoren habe ich zusätzlich zu Spyder die folgenden Editoren installiert und ausprobiert: Atom, Visual Studio Code, Vim, Idle. Während mir Vim und Idle bereits aus dem Kontext meiner Arbeit an der Hochschule Düsseldorf bekannt waren, da diese dort an meinem Rechner installiert sind, waren die anderen Optionen (Atom, Visual Studio Code) neu für mich und deren Auswahl ein Ergebnis der Betrachtung der entsprechenden Webseiten. Im direkten Vergleich erschienen mir sowohl Atom als auch Visual Studio Code deutlich schlanker und übersichtlicher und damit einfacher zu bedienen als Vim bzw. Idle. Insbesondere Visual Studio Code hat mir hierbei besonders gut gefallen, da ich die Bedienung als intuitiv erfunden habe und einige Optionen wie z.B. die direkte Integration von Git durchaus praktisch sind. In einem Ranking meiner Auswahl würde ich Vim aufgrund seiner Komplexität (bzw. verschiedenen Modi) auf dem letzten Platz sehen, knapp hinter Idle, welches mir optisch nicht so wirklich gefallen möchte. Der erste Platz geht dagegen an Visual Studio Code, knapp vor Atom, welches ebenfalls sehr intuitiv erscheint, letztendlich aber optisch aus meiner subjektiven Sicht nicht ganz an Visual Studio Code heranreicht. Da Spyder allerdings durch die Installation von Anaconda bereits installiert ist und ebenfalls gut für mich funktioniert, stellt sich die Frage, ob ein weiterer Editor sinnvoll erscheint. Letztendlich wird sich diese Frage wohl erst durch weiterführende Anwendung beantworten lassen. 

## 2. Eine Python-Bibliothek

### https://pypi.org/project/numpy/

Bei der Recherche nach einer interessanten Python-Bibliothek habe ich mir zunächst überlegt, welche Aufgaben ich in meinem Alltag mit Hilfe einer Python-Anwendung lösen könnte. Interessant wäre für mich z.B. eine Möglichkeit, Trainingsdaten aus dem Laufsport auswerten und grafisch darstellen zu können. Insbesondere eine Analyse der einzelnen Trainings- bzw. Intensitätsbereiche in Bezug auf physiologische Parameter wie z.B. Herzfrequenz-, Laktat-, oder Sauerstoffaufnahme-Werte wäre ein interessanter Anwendungsbereich. Die Erweiterung NumPy scheint die Möglichkeiten zu bieten, zuvor exportierte Trainingsdaten bzw. Auswertugen von Leistungsdiagnostiken miteinander in Bezug zu setzen, zu analysieren und auch grafisch darzustellen. Dabei ermöglich NumPy als Bibliothek sowohl die numerische Berechnungen als auch die mehrdimensionale Darstellung. Ein erster Versuch eine eigene Anwendung zu erstellen ist leider gescheitert - die Idee wird aber weiter verfolgt. 

## 3. Eine Fehlermeldung und Ihre Lösung

```"for ID in IDs:\n",
    "    full_url = base_url + ID\n",
    "    ID_json_data = urllib.request.urlopen(full_url).read()\n",
    "    ID_data = json.loads(ID_json_data)\n",
    "    print(ID)\n",
    "    print(ID_data[\"result\"][ID][\"pubdate\"])\n",
    "    print(ID_data[\"result\"][ID][\"title\"])\n",
    "    print()"```
 

Die größte Hürde bei der Lösung der Aufgabe war die Tatsache, dass die Daten, welche sich hinter der PubMed-ID verbergen, eine andere Struktur aufweisen, als die Daten, welche wir vorab über eine DOI aus CrossRef bezogen haben. Während der Befehl „doi_data.keys()“ bzw. darauffolgend „doi_data["message"].keys() im vorangegangenen Beispiel alle verfügbaren Metadaten ausgeworfen hat, waren in der vorliegenden Aufgabe lediglich zwei Auswahlmöglichkeiten gegeben, wobei sich die Metadaten hinter der ausgeschriebenen PubMed-ID verborgen haben. Diese Struktur, also die Notwendigkeit, eine Ebene tiefer zu gehen, sorgte letztendlich bei der Abfrage der Daten für diverse Fehlermeldungen, welche sich alle darauf bezogen, dass die vier gefragten IDs an die Stelle der zuvor explizit ausgewählten ID treten sollten. Die ID im Dateipfad musste also durch eine Variable ersetzt werden, welche die korrekte Ausführung der Schleife ermöglicht. Alle Fehlermeldungen deuteten explizit auf diese Stelle des Befehls, da mir die richtige Lösung erst nach mehrmaligen Probieren verschiedener Schreibweisen deutlich wurde. Fehlerquellen waren hier z.B. IDs statt ID oder „ID“ statt ID. Die richtige Lösung sah schließlich folgendenmaßen aus: print(ID_data["result"][ID]["pubdate"]). 

## 4. Was ist JupyterLab?

Bei JupyterLab handelt es sich um eine Weiterentwicklung von Jupyter Notebook, welche die Oberfläche von Jupyter Notebook um die Funktionalität bzw. die Integration eines Text-Editors erweitert. Während Juypter Notebook den eingegebenen Code nach jeder Zeile ausführt und durch die Umschaltung von Code auf Markdown auch jederzeit das Kommentieren und somit eine vollständige Dokumentation des Vorgehens ermöglicht, ergänzt JupyterLab die Bedienung in Form eines modularen Aufbaus. Dieser ermöglicht gleichzeitig die Darstellung verschiedener Erweiterungen, so z.B. auch die Ansicht eines klassischen Text-Editors. Damit verbindet JupyterLab die Möglichkeiten des Notebooks und Text-Editors in einer kombinierten Oberfläche. Ebenso lässt sich diese Oberfläche durch verschiedenen Erweiterungen individuell an die eigenen Bedürfnisse anpassen. Neben der Darstellung von Jupyter Notebook und des Text-Editors können so z.B. verschiedene Daten und Anwendungen parallel betrachtet und bearbeitet werden. JupyterLab vereint somit viele Anwendungen, welche für die Arbeit mit Dateien benötigt werden, in einer konfigurierbaren Benutzeroberfläche. 

