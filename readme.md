# @media tag in css

## Allgemeine Syntax des @media tag´s

> @media not|only *mediatype* and (*mediafeature* **and|or|not** *mediafeature*) {*CSS-Code*;}

**mediatyps**
|type 	|Beschreibung												|
|-------|-----------------------------------------------------------|
|all 	|für alle media type Geräte									|
|print 	|für drucker												|
|screen |für Computerbildschirme, Tablets, Smartphones, etc.		|
|speech	|für Bildschirmlesen										|

**keywords**
|keyword|Beschreibung												|
|-------|-----------------------------------------------------------|
|not	|Das Schlüsselwort "not" kehrt die Bedeutung einer gesamten Medienabfrage um.|
|only	|Das Schlüsselwort "only" verhindert, dass ältere Browser, die Medienabfragen mit Medienfunktionen nicht unterstützen, die angegebenen Stile anwenden. Es hat keine Auswirkungen auf moderne Browser.|
|and 	|Das Schlüsselwort "and" kombiniert eine Medienfunktion mit einem Medientyp oder anderen Medienfunktionen.|
***Alle sind optional. Wenn du jedoch "not" oder "only" verwendest, musst du einen Medientyp angeben!***

## Browser Support

|Google Chrome|Edge |Firefox|Safari |Opera|
|-------------|-----|-------|-------|-----|
|	  21	  |  9  |  3.5  |  4.0  |  9  |

## Allgemeine Breiten
- 1.) min.: 1125px
- 2.) min.: 980px bis 1125px
- 3.) min.: 760px bis 980px
- 4.) max.: 760px
- 5.) Handy in Portrait Modus: 320px 

#### Copy and Past code zum Anfang
> @media screen (min-width: 1125px) {*CSS-Code*}
> @media screen (min-width: 980px) and (max-width: 1125px) {*CSS-Code*}
> @media screen (min-width: 760px) and (max-width: 980px) {*CSS-Code*}
> @media screen (max-width: 760px) {*CSS-Code*}
**für Handy und Tablett**
> @media screen (orientation: portrait) and (min-width: 300px) and (max-width: 450px) {*CSS-Code*}
> @medis screen (orientation: portrait) and (min-width: 700px) and (max-width: 950px) and (max-height: 450px) {*CSS-Code*}

## Code-Beispiele mit Erklärung

#### Beschreiben eines Breiten oder höhen bereiches
**Breiten**
> @media screen and (min-width: 500px) and (max-width: 800px) {*CSS-Code*}

**Höhen**
> @media screen and (min-height: 500px) and (max-height: 800px) {*CSS-Code*}

#### Beschreiben von CSS Eigenschaften anhand der Ausrichtung des Viewports
> @media screen and (orientation: landscape) {*CSS-Code*}
> @media screen and (orientation: portrait) {*CSS-Code*}

Die Abfrage nach der Ausrichtung wird mit dem *mediafeature* "orientation" eingeleitet. Danach die Beschreibung ob *landscape* oder *portrait*
Dieses Feature ist wichtig für die aussehensbeschreibung von Websites am Handy.

#### Bescheibung von CSS Eigenschaften anhand der Farbeinstellung des Users (Darkmode)
> @media (prefers-color-scheme: dark) {*CSS-Code*}

In der Regel sind Websites meist hell gehalten, jedoch fragen viele User nach einem dunklem Design. Mit dem *mediafeature* prefers-color-scheme kann man einfach den Usern die Möglchkeit bieten ein dunkles Design der Website zu verwenden.

#### Verwenden einzelner CSS Dokumente für unterscheidliche Tags
> *< link rel="stylesheet" media="(min-device-width: 900px)" href="/css/stylesheet-900.css">*

Hiefür fügt man wie gewöhnlich ein Sylesheet in den Kopf eines HTML-Dokumentes ein, jedochmmit dem Zusatz media"...(...)".
am Ende wie gewöhnlich den Speicherort des Dokumentes.