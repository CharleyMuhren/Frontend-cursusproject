# Procesverslag
Markdown is een simpele manier om HTML te schrijven.  
Markdown cheat cheet: [Hulp bij het schrijven van Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

Nb. De standaardstructuur en de spartaanse opmaak van de README.md zijn helemaal prima. Het gaat om de inhoud van je procesverslag. Besteedt de tijd voor pracht en praal aan je website.

Nb. Door *open* toe te voegen aan een *details* element kun je deze standaard open zetten. Fijn om dat steeds voor de relevante stuk(ken) te doen.





## Jij

<details open>

  ### Auteur:
 Charley Muhren

  #### Je startniveau:
  Blauw

  #### Je focus:
 Surface plane
 
</details>





## Je website

<details open>
  

  ### Je opdracht:
  https://www.milli.agency/
  

  #### Screenshot(s) van de eerste pagina (small screen): 
 Milly agency (homepage)
  <img src="https://www.milli.agency/>


<img width="499" height="737" alt="Screenshot 2026-01-21 at 17 33 28" src="https://github.com/user-attachments/assets/a12c0b55-885f-41ce-97fe-9da20e344463" />





  #### Screenshot(s) van de tweede pagina (small screen):
  Work
  <img src="https://www.milli.agency/work)">

<img width="499" height="736" alt="Screenshot 2026-01-21 at 17 32 41" src="https://github.com/user-attachments/assets/881cd1cc-145d-4f46-a8c1-ac8780e1268e" />
<img width="501" height="731" alt="Screenshot 2026-01-21 at 17 32 33" src="https://github.com/user-attachments/assets/cf80053d-391b-40d4-bc41-9fdaed0da71d" />
<img width="500" height="734" alt="Screenshot 2026-01-21 at 17 32 18" src="https://github.com/user-attachments/assets/701bcab9-c868-42ff-b606-930555ee0677" />
<img width="499" height="739" alt="Screenshot 2026-01-21 at 17 32 11" src="https://github.com/user-attachments/assets/ccc1245a-7373-45a0-9d25-554fb98e48d7" />


  
 
</details>



## Toegankelijkheidstest 1/2 (week 1)

<details open>
Screenreader test:
De website komt op de volgende punten niet goed uit de screenreader test:  
De website lijkt in een Webflow gebouwd te zijn en er lijkt geen rekening gehouden te zijn met semantiek.  
De webside bevat geen headings en er zijn geen skip links. 

WCAG checklist:
1. Content: op zich is de content die er is helder, er wordt niet veel beschreven dus je moet het met vrij weinig informatie doen. De label, a en button elementen zijn beschrijvend en de teksten zijn links uitgelijnd.
2. Global code:

A. Ik heb de homepage getest met de HTML validator en daar komen 128 punten uit. Het zijn 5 punten die meerdere malen terugkomen:
- De melding  "Trailing slash on void elements has no effect and interacts badly with unquoted attribute values." komt veelvuldig voor en houdt in dat bij het gebruik van 'Void elements' (lege elementen zoals <img>, <br>, <input>, <meta>) er geen closing tag nodig is. De slash kan problemen geven bij unquoted attributes dus moet verwijderd worden.
- De waarschuwing "The type attribute is unnecessary for JavaScript resources." houdt in dat type="text/javascript" overbodig is. In HTML5 is JavaScript de standaard script-taal. Browsers gaan er automatisch vanuit dat een <script>-tag JavaScript bevat, tenzij je iets anders aangeeft. Weglaten levert schonere en modernere HTML op.
- De error 'Element style not allowed as child of element div in this context. (Suppressing further errors from this subtree.)'  betekent dat het 'style' element op een plek staat waar het niet mag, namelijk in de <body> tussen andere content. Een <style>-element mag alleen in de <head> van je document, in een <noscript> binnen de <head>. Het is het handigst om een aparte stylesheet te maken (is deze website gemaakt in Webflow want dan schijnt dit vaker voor te komen).
- De error "Attribute transform-origin not allowed on element div at this point." betekent dat "transform-origin" geen HTML-attribuut is voor een <div> maar een CSS-property dus dat het als zodaning naar de stylesheet moet worden verplaatst.
- De error "Duplicate ID w-node-_987fbb7e-48c6-1366-77d6-9c2152bf269b-7a4a2958" houdt in dat er twee keer dezelfde ID gevonden is op de pagina terwijl een ID maar één keer gebruikt mag worden.

B. <html lang="nl"> is aanwezig in broncode  
C. Elke pagina heeft unieke <title> in browser tabs  
D. De viewport meta tag heeft geen user-scalable=no of restrictieve maximum-scale
  

3. Keyboard:  
A. De focus is niet visueel gemaakt, je ziet niet wat je aan het doen bent.
B. De volgorde klopt aardig maar er wordt een link (naar 'Connect') overgeslagen.

4. Mobile and touch:  
A. Bij horizontale rotatie  valt de content buiten beeld.  
B. Je kan alleen verticaal scrollen (omhoog/omlaag), alle content past binnen de schermbreedte en er steken geen elementen uit aan de zijkant.  
C. De knoppen zijn groot genoeg om makkelijk te raken, je kan niet per ongeluk op de verkeerde knop tikken en de icons hebben genoeg "tap area".  
D. Er is genoeg ruimte tussen knoppen, je kunt scrollen zonder per ongeluk te klikken, er is genoeg ruimte rondom elk element.

5. Headings:  
A. Er zijn geen headings te vinden, alleen div's en 'a' elementen die linken naar andere pagina's.  
B. Er zijn dus ook niet meerdere H1 elementen te vinden.  
C. Ze zijn dus ook niet in een logische volgorde geschreven.  
D. Er worden dus ook geen heading levels overgeslagen.  

6. Lists:   
Er bevinden zich geen list items op deze pagina, geen ul, ol en dl/

7. Images:  
De homepage bevat geen afbeeldingen, wel een video. Op de andere pagina's staan wel afbeeldingen die een alt text bevatten.  
En in het geval van een decoratieve afbeelding bevatten ze null alt (empty) attributen. Er staat een complexe afbeelding op (een grafiek) met een alt die niet de tekst uit de afbeelding bevat.  De afbeeldingen die tekst bevatten, zoals het logo, bevatten wel de tekst in de alt description.

8. Media (Video and Audio):  
De video's op de website zijn embedded en worden niet vanzelf afgespeeld. Het is niet bij alle video's mogelijk de ondertiteling in YouTube aan te zeten maar als het niet kan, is het ook niet nodig want die video's bevatten alleen beeld en muziek. Bij de video's met gesproken tekst is ondertiteling wel mogelijk.Ik kan nergens een transcript vinden.


9. Controls:  
De a elementen worden gebruikt voor links.  
Het is op de mobiele versie op het eerste gezicht lastig om te zien wat wel en niet klikbaar is.  
Op de desktop versie zie je wel dat de verschillende vlakken met de navigatie (work, about, community en contact) klikbaar zijn doordat de vlakken van kleur veranderen bij de hover. De pijltjes op de 'work' pagina zijn alleen door de vorm (een pijl) duidelijk klikbaar.  
Er zijn nergens focus states te zien.  
Voor buttons zijn geen button elements gebruikt.  
Er zijn geen skip-links gebruikt.  
Er wordt gebruik gemaakt van target_blank maar zonder indicator. 

10. Appearance:  
De website heeft geen dark mode.  
High-contrast mode wordt niet gesupport.
Tekst grootte op 200 % zetten, zorgt ervoor dat de navigatie breekt, content verdwijnt of wordt afgesneden en buttons elkaar overlappen.  
Kleur is niet de enige manier waarop informatie wordt overgebracht, zo hebben inputvelden labels.

11. Animation:   
Over het algemeen zijn de animaties in een goed tempo. Hun video reel flitst wel erg.
Video's kunnen gepauzeerd worden (de video's zijn embedded en staan op YouTube).  
Met de optie 'prefers-reduced motion' aan, blijven de animaties hetzelfde!  

12. Color controst:  
Het contrast is over het algemeen goed tot heel goed.  
Het zwart op het geel is goed en de kleur bij het selecteren van tekst is ook geel waardoor ook dan de tekst goed te lezen is. 

</details>


  ### Bevindingen
  <details open>
  Lijst met je bevindingen die in de test naar voren kwamen:

</details>



## Breakdownschets (week 1)

<details open>
  <summary>uitwerken na afloop 3<sup>e</sup> werkgroep</summary>

  ### de hele pagina: 
  <img src="readme-images/dummy-plaatje.jpg" width="375px" alt="breakdown van de hele pagina">

  ### dynamisch deel (bijv menu): 
  <img src="readme-images/dummy-plaatje.jpg" width="375px" alt="breakdown van een dynamisch deel">

  ### wellicht nog een dynamisch deel (bijv filter): 
  <img src="readme-images/dummy-plaatje.jpg" width="375px" alt="breakdown van nog een dynamisch deel">

</details>





## Voortgang 1 (week 2)

<details open>
  <summary>uitwerken voor 1<sup>e</sup> voortgang</summary>

  ### Stand van zaken
  hier dit ging goed & dit was lastig (neem ook screenshots op van delen van je website en code)


  ### Agenda voor meeting
  samen met je groepje opstellen

  | student 1      | student 2          | student 3    | student 4        |
  | ---            | ---                | ---          | ---              |
  | dit bespreken  | en dit             | en ik dit    | en dan ik dat    |
  | en dat ook nog | dit als er tijd is | nog een punt | dit wil ik zeker |
  | ...            | ...                | ...          | ...              |


  ### Verslag van meeting
  hier na afloop snel de uitkomsten van de meeting vastleggen

  - punt 1
  - punt 2
  - nog een punt
  - ...

</details>





## Voortgang 2 (week 3)

<details>
  <summary>uitwerken voor 2<sup>e</sup> voortgang</summary>

  ### Stand van zaken
  hier dit ging goed & dit was lastig (neem ook screenshots op van delen van je website en code)


  ### Agenda voor meeting
  samen met je groepje opstellen

  | student 1      | student 2          | student 3    | student 4        |
  | ---            | ---                | ---          | ---              |
  | dit bespreken  | en dit             | en ik dit    | en dan ik dat    |
  | en dat ook nog | dit als er tijd is | nog een punt | dit wil ik zeker |
  | ...            | ...                | ...          | ...              |


  ### Verslag van meeting
  hier na afloop snel de uitkomsten van de meeting vastleggen

  - punt 1
  - punt 2
  - nog een punt
- ...

</details>





## Toegankelijkheidstest 2/2 (week 4)

<details>
  <summary>uitwerken na test in 9<sup>e</sup> werkgroep</summary>

  ### Bevindingen
  Lijst met je bevindingen die in de test naar voren kwamen (geef ook aan wat er verbeterd is):

</details>





## Voortgang 3 (week 4)

<details>
  <summary>uitwerken voor 3<sup>e</sup> voortgang</summary>

  ### Stand van zaken
  hier dit ging goed & dit was lastig (neem ook screenshots op van delen van je website en code)


  ### Agenda voor meeting
  samen met je groepje opstellen

  | student 1      | student 2          | student 3    | student 4        |
  | ---            | ---                | ---          | ---              |
  | dit bespreken  | en dit             | en ik dit    | en dan ik dat    |
  | en dat ook nog | dit als er tijd is | nog een punt | dit wil ik zeker |
  | ...            | ...                | ...          | ...              |


  ### Verslag van meeting
  hier na afloop snel de uitkomsten van de meeting vastleggen

  - punt 1
  - punt 2
  - nog een punt
  - ...

</details>





## Eindgesprek (week 5)

<details>
  <summary>uitwerken voor eindgesprek</summary>

  ### Je uitkomst - karakteristiek screenshots:
  <img src="readme-images/dummy-plaatje.jpg" width="375px" alt="uitomst opdracht 1">


  ### Dit ging goed/Heb ik geleerd: 
  Korte omschrijving met plaatjes

  <img src="readme-images/dummy-plaatje.jpg" width="375px" alt="top">


  ### Dit was lastig/Is niet gelukt:
  Korte omschrijving met plaatjes

  <img src="readme-images/dummy-plaatje.jpg" width="375px" alt="bummer">
</details>





## Bronnenlijst

<details open>
  <summary>continu bijhouden terwijl je werkt</summary>

  Nb. Wees specifiek ('css-tricks' als bron is bijv. niet specifiek genoeg). 
  Nb. ChatGpT en andere AI horen er ook bij.
  Nb. Vermeld de bronnen ook in je code.

  1. bron 1
  2. bron 2
  3. ...

</details>
