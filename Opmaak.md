# Architectuur DocShare toepassing

*(Verwachtingen voor elke paragraaf staan tussen haakjes. Laat ze staan zolang dit document in ontwerp-fase is maar denk eraan ze allemaal te verwijderen tegen versie 1.0. Denk eraan dat vanaf versie 1.0 een document volledig moet zijn. Echt finaal is een document natuurlijk nooit. Gelieve de structuur van dit document niet te veranderen, om zo het nalezen ervan te vergemakkelijken. Vul de lege paragrafen aan maar wees niet bevreesd om de vooringevulde tekst aan te passen of zelfs te vervangen. Er wordt verwacht dat het hele document tussen de 2500 en 5000 woorden bevat tegen v1.0.)*

<center>
Opdracht voor Design Patterns & ICT Architecture

2018-2019

<small>Voornaam_1 Naam_1<br>Voornaam_2 Naam_2</small>
</center>

---

## Samenvatting

*(Hier moet een samenvatting komen van dit document. De samenvatting kan je pas schrijven op het allerlaatst wanneer er een volledig ontwerp is voor alle andere paragrafen. De samenvatting moet dan ook het ganse document samenvatten en niet enkel de probleemstelling of doelstelling. Let op, ook de samenvatting moet best nog eens ge-reviewed worden alvorens versie 1.0 te publiceren.)*

## Objecten, Actoren en Activiteiten

Dit zijn de objecten die centraal staan in de toepassing:

- *Idee* - Origineel idee of geïntegreerd begrip
- *Opdracht* - Een opdracht op Digitap
- *Document* - Een document dat ingeleverd dient te worden als onderdeel van een *Opdracht*
- *Sjabloon* - Een sjabloon voor het in te leveren *Document*
- *Paragraaf* - Een paragraaf binnen een *Document*
- *Commentaar* - Een opmerking of aanmerking op een *Document*, een *Paragraaf* of een onderdeel van een *Paragraaf*
- *Punt* - Een score op een onderdeel of het geheel van het *Document*
- *Plagiaat* - Een kantitatieve maat voor de originaliteit van een *Document*

Dit zijn de actoren die een rol hebben in de DocShare toepassing:

- **Student** - een student bij de AP
- **Lector** - iemand die de opdracht opstelt en de evaluatie uitvoert
- **Reviewer** - iemand die een *Document* nakijkt en *Commentaren* levert

Hier volgen de definities van de relevante activiteiten:

- ***Ideevorming*** - Het vormen van een *Idee*
- ***Schrijven*** - Het vastleggen van een *Idee* in een *Document*
- ***Inleveren*** - Het inleveren van een *Document*
- ***Nakijken*** - Het voorzien van *commentaren* op een *Document*
- ***Evalueren*** - Het voorzien van een ***Ingeleverd*** *Document* van een *Punt*
- ***Terugsturen*** - Het terugsturen van een ***Nagekeken*** *Document* van *Reviewer* naar *Student*
- ***Analyseren*** - Het automatisch extraheren en analyseren van tekst en afbeeldingen uit een *Document*

## Probleemstelling

Nu worden *Opdrachten* via het Digitap systeem afgehandeld. Indien er *Documenten* moeten ***Nagekeken*** worden, worden deze ***Ingeleverd*** als PDF bestanden, ***Nagekeken*** door een **Reviewer** en ***Teruggestuurd***. Bij het ***Evalueren*** wordt elk *Document* door de **Lector** nog eens grondig ***Nagekeken*** en voorzien van *Punten*. Bij grote groepen studenten (n > 50), kan het dagen duren om de ***Evaluatie*** van al de *Documenten* af te ronden. Hoewel het PDF-formaat veel voordelen heeft, vnl naar ondersteunbaarheid toe (cross-platform), is het niet geschikt voor het ***Nakijken*** of het ***Analyseren*** van *Documenten*. Eén van de toekomstige doelstellingen is bijvoorbeeld om de ingestuurde *Documenten* te onderzoeken op *Plagiaat*, maar daarvoor is automatische tekst extractie noodzakelijk. Een tweede voorbeeld is om in de toekomst eerder gebruikte *Commentaren* snel op te halen en tijdens het ***Nakijken*** te hergebruiken. Een derde voorbeeld is om de verscheidene versies van een ingestuurd *Docment* eenvoudig met elkaar te kunnen vergelijken om zo de evolutie van een *Document* in kaart te brengen. Tenslotte, maakt PDF het moeilijk om *Studenten* een voorafgesproken *Sjabloon* te laten naleven. Een sjabloon dat strikt nageleefd wordt vereenvoudigt immers de bovengenoemde activiteiten. Kort samengevat kan men stellen dat de huidige manier om *Documenten* ***Na te kijken*** traag en inefficient is. 

## Doelstelling

*(De doelstelling draait rond het opsommen van de vereisten. Het voorstel is om letterlijk de vereisten te nummeren, zodat je er achteraf naar kan verwijzen. Denk erom: een functionele vereiste is niet een oplossing, het is enkel de noodzaak om iets te kunnen doen. Je verwijst hier dus in principe niet naar enige technologie. Bijvoorbeeld, je zegt: de **Lector** moet de mogelijkheid hebben om een *commentaar* uit de lijst van beschikbare historische commentaren te kiezen, maar je zegt niet: de **Lector** drukt op CTRL-L en via een query naar de DB wordt een lijst van *commentaren* opgehaald.)*

### Functionele vereisten

*(Hier gaat het specifiek over de functionele vereisten die beschrijven hoe de applicatie moet functioneren. Als dit niet goed zit kan de oplossing dat ook niet zijn. Opgelet: 'functioneel' betekent niet dat je vaag moet blijven. Bijvoorbeeld: De lijst van *Historische Commentaren* is gesorteerd volgens hun relevantie; zie nota # voor het berekenen van relevantie.)*

### Algemene, niet-funtionele vereisten

*(Hier volgen de niet-functionele vereisten. Uiteraard kunnen deze onrechtsreeks wel een ernstige impact hebben op het functioneren van de applicatie, alleen zijn ze zelf niet functioneel van aard. Probeer elk paragraaf aan te vullen, vul desnoods 'Niet van toepassing' in maar enkel indien dit echt zo is!)*

#### Toegankelijkheid - Accessibility
#### Beschikbaarheid - Availability
#### Configureerbaarheid - Configurability
#### Uitbreibaarheid - Extensibility
#### Performantie - Performance
#### Onderhoudbaarheid - Maintainability
#### Schaalbaarheid - Scalability
#### Beveiliging - Security
#### Ondersteunbaarheid - Supportability
#### Testbaarheid - Testability
#### Gebruiksvrindelijkheid - Usability

## Architectuurstijlen en -patronen

(Beschrijf hier, in 100-500 woorden, de architectuur stijl(en) die je hebt gekozen. Dit is belangrijk om te kunnen communiceren met andere architecten. Zij kunnen daar dan meteen allerhande consequenties aan koppelen die eigen zijn voor die stijlen. Sommige subsystemen hebben de ene stijl en andere subsystemen hanteren misschien een andere stijl. Subsystemen kunnen ook om een combinatie gaan van meerdere stijlen, of een versmelting. Je vindt een lijst van stijlen terug op deze Wikipedia pagina: https://en.wikipedia.org/wiki/List_of_software_architecture_styles_and_patterns. Zoek op wat deze stijlen betekenen (verdeel het werk) en zoek meteen op of er voor de stijlen bekend is wat de voor- en/of nadelen zijn, de voorwaarden om effectief te zijn enz.... Kijk dan welke stijlen er bij jouw subsystemen passen. Geef hier, in een paar woorden - je eigen woorden! - wat er kenmerkend is voor de gekozen stijlen en waarom je denkt dat ze van toepassing zijn voor dit project.)

## Architectuur

(Hier komen de oplossingen die één voor één moeten matchen met één of meerdere (niet-)functionele vereisten (gebruik de nummers!). Dus zeker niet onbelangrijk! Hier mag je volledig technisch gaan! Je krijgt de vrijheid in je keuze van  programeertaal/infrastructuur/... maar denk eraan: de bedoeling is dat de toepassing echt moet werken! Dit is een technisch onderdeel, dus wees efficient in je schrijven. Hier wordt hoge informatie dichtheid vewacht! Geen gelul! Niet zeveren! Maar dat alle informatie aanwezig is voor een junior ontwikkelaar om te kunnen ontwikkelen.)

### Business View
### Functionele View
### Informatie View
### Applicatie View
### Infrastructuur View

## Risico-analyse

*(Je systeem is af, proficiat! Maar wat als er iets fout loopt. Voer hier je risico-analyse uit. Hou je niet bezig met voordehand liggende items die echt geen gevaar vormen!)*

## Proof-of concept

*(Deze paragraaf moet nog niet klaar zijn tegen 1.0. Hier moet je de opdrachtgever kunnen overtuigen dat het plan wel eens écht zou kunnen werken. Geen tijd steken in het vanzelfsprekende en dus enkel die dingen die als hoog-risico uit de risico-analyse komen.)*

## Afkortingen

- PDF - Portable Document Format

## Referenties

*(Wees fair en refereer naar andermans werk. Als jij origineel werk creëert zou je dat ook willen, toch! Maar, a.u.b. geen referenties naar het werk van een collega, of naar de slides van de lector of zoiets. Enkel refereren van gepubliceerd materiaal, lieft peer-reviewed werk)*

| |Referentie|
|:-|:--------------------------------------------|
| <sup>1</sup>|Naam1 V, Naam2 V, ...NaamN V (YYYY) Titel artikel/Boek. Blad/Uitgever. (Uitgave:) p###-###.|

*(Succes!)*
