### 1 - Overview the exercise Files:
#### 1 - The VS Code UI:
* code = VS Code über Terminal öffnen
* ganz links = Viewbar
* **STRG+SHIFT+e** - zum File-Explorer weckseln 
* **STRG+SHIFT+F** - Suchen in Dateien
* **STRG+SHIFT+G** - Git-Teil öffnen
* **STRG+SHIFT+D** - Debugger öffnen
* **STRG+SHIFT+X** - Extentions-Teil öffnen
* **STRG+SHIFT+P** - Command Palet (Befehlszeile) öffnen
* **STRG+K+Z** oder Anzeigen > Darstellung - Zen-Modus = nur Datei wird angezeigt <-Verlassen = ESC
* **STRG+K+F** (Rechtslick -> Formatierer) = Formatierer aufrufen
* **STRG+i** - ganze Zeile auswählen
#### 2 - Basic editing:
* **STRG+/C/V/X** = kopiert ganze Zeile wenn nichts ausgewählt
* **STRG+[; STRG+]** - Tab links/rechts ([/] = **ALT GR**) <- funktioniet nicht im deutschen 
* **STRG+i** - ganze Zeile auswählen -> weitere Zeilen auswählen = mehrmals **STRG+i** klicken
* **ALT+Pfeil** nach/oben/unten = Zeile nach oben/unten verschieben
* Text auswählen -> **STRG+SHIFT+P** -> run selected ... - Auswahl im Terminal ausführen
* **STRG+SHIFT+Pfeil nach oben/unten** - im Termianl nach oben/unten scrollen

#### 3 - The integrated terminal
* **STRG+`** - Terminal öffnen
* Terminal hat die gleichen Rechte, wie die der aktueller User
#### 4 - integrated Source Control:
* VS Code findet automatisch, ob git installiert => kann installierten git benutzen
* wenn man .git-Ordner hat => Git-Symbol ganz Link wird aktive + verfolt Änderungen
* Wenn man Änderungen zu Vorher ansehen will => auf das Git-Symbol klicken -> auf veränderte Datei klicken => git zeigt änderungen an (Working vs. HEAD)
    *  Buttons oben rechts ansehen
    * im Editor:
        * grün = neue Zeile
        * blau = veränderte Zeile
        * rot (Dreieck) = gelöschte Zeile
    * im Git-Symbol:
        * *+/-* (Rechtsklick + Stage/Unstage) = zu/aus Stage/(git add / git revert)
        * oben kann man Kommentar eingeben + Häckchen klicken /STRG+Enter = git commit /
            *+*-Symbol mit Drei Punkten = Weitere git Commands (push, pull)

### 2 -  Customizing VS Code:
#### 1 - Configuring preferences:
* Datei -> Einstellungen <- json-Datei (inzwischen kein json, den man verändern kann)
    * oben im Suchfeld eingeben was man verändern will
* Es gibt Benutzereinstellungen (Allgemein) und Arbeitsbereicheinstellungen
* **STRG+SHIT+P** (Befehlspalette) -> preferences -> Config language spezific .. -> Sprache auswählen 
    * in settings.json wird Zeile für Sprache hinzugefügt
#### 2 - Setting keyboard shortcuts:
* Datei -> Einstellungen -> Tastenkombinationen
* Drei Sachen: Shortcut -> Befehl -> Wenn-Option (Zeitpunkt) = wann Shortcut ausführbar sein soll (Optional, Default = Immer)
* Es gibt Erweiterunngen, die shortcuts mit Shortcuts aus anderen Editoren ersetzen
#### 3 - Using extensions:
* https://marketplace.visualstudio.com = nach Erweiterungen suchen -> Visual Studio Code - Tab auswählen -> Erweiterungen durchsuchen

#### 4 - Essential extensions:
* für Web:
    * HTML Snippets
    * jQuery Code Snippets <- fangen mit jq... an
    * Beautify
    * Express = Server
    * REST Client = testen HTML- Requests/Responses (GET/POST-Anfragen) <- hat viele Einstellungen
        * manche Extentions-Befehle kann man über Befehlspalette ausführen

#### 5 - Working with snippets:
* Quadrat in IntelliSence = Snippets
    * mit Tab kann man zu nächsten Parameters des Snipptes wechseln
* Datei -> Einstellungen -> Benutzercodeausschnitte -> Sprache auswählen <- es wird ein .json geöffnet:
    ```
    "document.querySelector : { <- Snipptename
        "prefix" : "dqs", <- wenn man dqs eingibt => Snippet wird nangezeigt
        "body" : [ <- was soll ausgeführt werden
            "var ${1:elem} = document.querySelector("${2:expression});"
        ],
        "description" : "Query for an element using CSS syntax" 
    }
    ```

#### 6 - Color and icon themes:
* Datei -> Einstellungen -> Farbdesign <- PupUp mit den Farbauswahlen
* Erweiterungen -> themes -> Installieren <- im Farbdesign auswählen
* Datei -> Einstellungen -> Datei-Symboldesign  <- kann man Weitere im Marketplace kaufen

### 3 - Using the Editor:
#### 1 - Files Folders and projects:
* Ordner - wie Workspace behandelt
* 1 Klick - Preview
* **STRG+TAB** - zwischen Tabs wechseln
* **STRG+ALT+T** - alle TABS außer aktuellen schließen.
* **TAB** oder Datei Rechtsklicken -> im Dateiexplorer öffnen
* Datei rechtsklicken -> im Terminal öffnen => Terminal im Ordner der Datei öffnen
#### 2 - Side by side editing:
* **STRG+\\** - Split die gleiche Seite
* **STRG+ALT+1** - Split nach unten
* **STRG+1/2/3** - zwischen Splits wechseln
#### 3 - IntelliSence
* **TAB / Enter** - IntelliSence auswählen
* **ECS** - IntelliSence ignorieren
* **STRG+Leertaste** - IntelliSence manuell aufrufen
    * kreis -> Kreis - IntelliSence
    * blaue Kiste - Variable
    * purpure Kiste = Funktion
    * Quadrat mit Punkten unten = Snippet
        * siehe Dokumentation von VS Code
#### 4 - Finding and replacing
* **STRG+F** - suchen
* Wort auswählen - **STRG+G** 
* im PopUP von Suchen kann man Groß/Klein einstellen usw 
* **STRG+H** - suchen + ersetzen
* **STRG+SHIFT+F** - in Dateien suchen -> mit Pfeil nach unten/oben - Treffer durchlaufen
* **STRG+SHIFT+J** - Suche mit Parametern 


### 4 - Advanced Editing:
### 1 - Editor features:
* HOT Exite = speichert letzten Stand beim Beenden 
    * in den Einstellungen
    * Autosave <- in Einstellungen
    * in Einstellungen "format" eingeben -> einstellen. man braucht aber Format-Erweiterung dafür
#### 2 - Web code editing:
* **STRG+//** = Alles kommentieren
* Dokumentar-Kommentare = /** eingeben -> Tab -> mit Tabs durch Parameter durchklicken (Bsp: JS)
* Befehl = markdown: Voschau aktualisieren => z.B für HTML Vorschau anzeigen.
* Support von Emmit-Snippets:
    * Emmet-Seite: https://docs.emmet.io = html durch emmet erstellen
        * Bsp:
        ```
        nav#pageNav.cf>ul>(li>a)*5 -> Tab klicken => HTML wird daraus erstellt
        ```
#### 3 - Navigating code:
* **STRG+G** - Zeilennummer eingeben
* **STRG*SHIFT+O** - zum Code-Schlüsselwort wechseln
* **STRG+P** - Liste der Datei anzeigen -> mit Pfeilen navigieren

#### 4 - Using multiple selections:
* Auswahl
    * STRG+D - Wort auswählen auf dem Curser steht
    * mehrmals **STRG+D** - zweites gleiches Wort noch
    * **STRG+SHIFT+l** - alle Wörter wie das ausgewählte auswählen
    * **STRG*ALT+Pfeil** nach oben/unten = Curser an gleichen Stelle oben/unten machen
    * **STRG+SHIFT <-/->** - Auswahl erweitern/verkleinern

#### 5 - JSON and schemas:
* für *bower.json* ist schon Schema eingebt => IntelliSence vorhanden.
* *schemastore.org/json* - Schemas für verschiedene Manifest-Dateien:
    ```
    {
        "$schema" : url_für_schema, <- IntelliSence für diesen json wird vorhanden sein
    }
    Einstellungen -> json suchen -> json Schemas -> "fileMatch" : [
        manifest.json"
    ],
    "url" : "url_für_schema" 
    ```
* wenn man eine Datei *manifest.json* nennt => wird obige IntelliSence verwendet.
