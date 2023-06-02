# Introductie

In deze module willen we je graag verbazen met techniek, succes en ongemak rond *kunstmatige intelligentie* (KI). We hopen natuurlijk dat je hierna niet kunt wachten om met de rest van de module te beginnen om meer te weten te komen over dit interessante en best wel actuele onderwerp. We beginnen de verbazing met beeldherkenning voor de leuk, daarna geven we een voorbeeld van een serieuzere succesvolle toepassing en zadelen we je op met wat ongemak. Als laatste presenteren we het doel van de cursus.

## Quick draw

Hoeveel heb je nodig om iets te herkennen? Misschien ken je het spel *Pictionary*. In dit spel moet je een tekening maken bij een woord en je teamgenoot moet dit woord dan raden. Speel het spel hieronder en laat je verbazen hoe goed AI als teamgenoot in dit spel is.

:::{figure} figs/quick-draw-google.png
:width: 400

Link naar het spel: [Quick, Draw!](https://quickdraw.withgoogle.com)

:::

Geweldig toch? Misschien heb je nu dezelfde vragen als wij hadden:

- Hoeveel figuurtjes zijn er gebruikt om jouw tekeningen mee te vergelijken?
- Was de app goed in het herkennen? Lag dat aan jouw tekenkunsten of aan de slimheid van de app?
- Denk je dat het ingewikkeld is om zo’n spel te bouwen? Leg uit waarom wel/niet.

Quick draw is een open project. Iedereen kan met de code en de dataset aan de slag. Volg [deze link](https://github.com/googlecreativelab/quickdraw-dataset) en geef het antwoord op de eerste vraag. Het antwoord op de tweede vraag is dat er een neuraal netwerk is ingezet om eerst van 50 miljoen tekeningen te leren. Daardoor is de app in staat heel snel te bepalen tot welke groep jouw tekening behoort, zoals bijvoorbeeld een bal of een fiets. Het indelen van een object bij een groep (categorie, klasse) op basis van vergelijkbare eigenschappen noemt men classificeren. Maar hoe doet zo'n netwerk dat dan?

In deze cursus kun je na een algemeen deel een pad kiezen waarin je je kunt verdiepen in de achterliggende technieken.

# Succesverhaal

Er zijn vele terreinen waar kunstmatige intelligentie een groot succes is, waaronder de gezondheidszorg. Het diagnosticeren van ziekten of aandoeningen aan de hand van beeldmateriaal is niet altijd even makkelijk, voor zowel mens als machine. Het bundelen van menselijke intelligentie en kunstmatige intelligentie leidt in veel gevallen tot succes. Het volgende filmpje is een voorbeeld hiervan (Tip: je kunt via de instellingen onderin de ondertiteling laten vertalen naar het Nederlands.)

<iframe width="560" height="315" src="https://www.youtube.com/embed/Mur70YjInmI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

In het filmpje zie je dat de radiologen trainingsdata moeten vormgeven. In het Quickdraw voorbeeld zijn er 50 miljoen tekeningen gebruikt met weinig tot geen overbodige informatie. In de video zag je beelden voorbij komen met veel meer informatie, maar slechts een klein deel van deze informatie was ook daadwerkelijk nuttig. Bij het zien van het filmpje, kwamen bij ons gelijk een paar vragen naar boven. Hopelijk bij jou ook.

- Is dit een toepassing die voor de patiënt voordelig is?
- Is dit een toepassing die de zorg duurder maakt?
- Hoeveel voorbeelden heeft de KI in de video gezien?
- Kan de KI bijleren? Er waren situaties dat de KI niets zag maar zes radiologen wel.

De eerste vraag is natuurlijk positief te beantwoorden. Hoe beter de detectie, des te sneller een diagnose gesteld kan worden. Ook de laatste vraag is te beantwoorden met "ja". We kunnen de beschikbare dataset uitbreiden met de niet goed geclassificeerde beelden en daarna de applicatie opnieuw trainen. Dit hertrainen is trouwens niet een garantie dat daarna de diagnose juist gaat zijn. Het grote voordeel is dat alle radiologen die de applicatie gebruiken, tegelijk de nieuwe versie kunnen gebruiken. Er hoeven geen duizenden radiologen op cursus om de nieuwe diagnoses te leren begrijpen.

In deze cursus kun je na het algemene deel een pad kiezen waar je meer gaat nadenken over de toepassingen van kunstmatige intelligentie, dan over de techniek erachter.

# Gevaren

Bekijk de onderstaande video van *The Economist* over controle met behulp van KI.

<iframe width="560" height="315" src="https://www.youtube.com/embed/lH2gMNrUuEY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Hmm..., ook hier komen bij ons vragen naar boven:

- Is de informatie in de video juist?
- Als dat zo is, kunnen er naast de goede dingen van gezichtsherkenning ook de negatieve dingen, zoals de staatscontrole, naar onze samenleving komen?
- Of erger: is er hier al staatscontrole met behulp van KI?
- In welke andere landen gebeurt dit ook?

Klakkeloos kunstmatige intelligentie inzetten is geen goed plan. Ook in Nederland komt geautomatiseerde verwerking van [beelden uit de publieke ruimte voor](https://bewijs-in-strafzaken.nl/anpr-automatische-kentekenherkenning/). Aan welke ethische voorwaarden moet KI voldoen? Daar moet iedereen iets over weten, dus komt het in het algemene deel van deze cursus aan bod. Ook is er de mogelijkheid in deze cursus om je verder te verdiepen in de sociale en ethische aspecten van KI. 

# De module

De module kunstmatige intelligentie, waar je nu bent aanbeland, heeft als hoofddoel je bewust te maken van de veelheid van technieken die in dit deel van computertechnologie aanwezig zijn. Daarbij willen we je laten zien wat voor moois deze technieken te bieden hebben. De eerste twee voorbeelden hebben je hopelijk al warm doen lopen. Het zijn echter allemaal technieken die gebaseerd zijn op het menselijke brein. We moeten daarom goed nadenken over de gevolgen van het toepassen van deze technieken. Niet alleen is het menselijke brein niet onfeilbaar, zelfs met goede intenties kan er toch iets goed fout gaan. Er zijn ook menselijke breinen die iedere kans aangrijpen om het eigen gewin boven dat van een ander te plaatsen, bijvoorbeeld dictators en criminelen. Het derde voorbeeld geeft een beeld van een situatie waartegen we als samenleving echt iets moeten doen.

Sommigen van jullie willen misschien graag met de technieken aan de slag, anderen willen zich juist meer in de maatschappelijke kant verdiepen. Daarom hebben we ervoor gekozen om in deze module beide onderwerpen aan bod te laten komen. De module verlangt een inspanning van ongeveer 8 lesweken. Het lesmateriaal voor de eerste vier weken moet een basis vormen waarmee iedereen ons hoofddoel bereikt. De laatste vier weken staat jouw eigen interesse centraal. Zoek je meer verdieping in de technieken, of wil je juist meer aandacht geven aan de ethische kant van de zaak?

## Algemeen deel

Het algemene deel biedt een stukje geschiedenis en de huidige stand van zaken van kunstmatige intelligentie aan. Er is een overzicht van technieken en waar die in de wereld worden toegepast. Je leert nadenken over de betekenis van kunstmatige intelligentie voor personen en de samenleving. KI wordt door gegevens gestuurd en je leert een aantal simpele technieken die inzicht geven in de manier waarop KI leert.

[1. Achtergrond](https://www.notion.so/1-Achtergrond-013c5e50dbaa45e186ec6d21c040a3db)

[2. Ethiek](https://www.notion.so/2-Ethiek-fea038c7c3ad4ff5a846ffe7765c7aeb)

[3. Technieken](https://www.notion.so/3-Technieken-4cf53c6234f5447e8fd90a2ba3361c81)

## Verdiepende deel

Heb je de stof uit het algemene deel doorgewerkt, dan ga je zelf op onderzoek uit. Je bent in het algemene deel vast een aantal onderwerpen tegengekomen waar je meer over wilt weten. Er zijn voor jou al een aantal opdrachten verzonnen om de verdieping te starten, vul die aan met eigen vragen en beschrijf wat je geleerd hebt in een verslag.