# Multi-agentsystemen

## Wat is een multi-agentsysteem

Een andere vorm van kunstmatige intelligentie is die van een **multi-agentsysteem (MAS)**. In de naam multi-agentsysteem zit het woord ‘multi’, dat staat voor meervoudig. Een multi-agentsysteem is dus letterlijk een systeem met meerdere agents. Multi-agentsystemen zijn gecomputeriseerde systemen die taken verrichten die niet of moeilijk door een individuele agent of een allesomvattende applicatie kan  worden gedaan.

Multi-agentsystemen overlappen met het concept **agent-based modelleren (ABM)**. Het doel van een agent-based model is het verkrijgen van inzicht in het gedrag dat agents door interactie met elkaar vertonen.  De agents in een agent-based model hoeven niet noodzakelijk intelligent te zijn en er wordt meestal gekeken naar verklaringen op basis van simpele regels in natuurlijke systemen (zwerm gedrag van vogels, groepsgedrag van mensen, mierensnelwegen). Multi-agentsystemen worden juist ontwikkeld om technische problemen op te lossen. Dus niet om gedrag te verklaren maar om gedrag te verkrijgen, Toepassingsgebieden voor MAS zijn onder andere [online handel](https://research.tue.nl/nl/publications/simulation-of-a-trading-multi-agent-system), [handelen bij rampen](https://www.ics.uci.edu/~dsm/papers/2006/multiagent06.pdf), [serious gaming](https://www.uu.nl/en/research/artificial-intelligence/intelligent-systems/research-themes/engineering-multi-agent-systems) en [surveillance](https://users.ba.cnr.it/issia/iesidd98/papers/DiPaola-IAV_2010.pdf). Ben je meer  of ook geïnteresseerd in het zoeken naar de oorzaak van gezamenlijk gedrag van organismen (ABM) dan is de verdiepingsmodule modelleren bij het keuze thema computational science iets voor jou. Later in deze sectie bekijken we aan aantal agent-based modellen die in multi-agentsytemen worden gebruikt.

## Gedrag

In de introductie in AI technieken hebben we het begrip agent geïntroduceerd als een zelfstandig functionerend deel van een AI applicatie. Functioneren betekent hier het tonen van gedrag. Een zelfrijdende auto is een agent van een AI applicatie die getraind is om zelfstandig te handelen in het verkeer. Het hele verkeer bestaat uit agents (let wel een menselijk persoon is ook een agent). De auto heeft als doel om personen in de auto veilig van plek A naar plek B te brengen. De auto neemt de huidige verkeerssituatie (is omgeving) waar. De auto zal handelen ten opzichte van de verkeerssituatie in het belang van de inzittenden van de auto. Stel dat er twee zelfrijdende auto’s op elkaar afrijden. Beide zelfrijdende auto’s zullen dan waarschijnlijk uitwijken om een botsing te voorkomen. In dit geval overlappen de doelen van deze agents en vertonen ze **coöperatief** gedrag.


Het is zeker niet zo dat de doelen van agents tot samenwerking leiden. Bij online handel is het doel van jouw agent om de winst voor de eigenaar van de agent te vergroten. Als er een vaste hoeveelheid aandelen in omloop is dan is er concurrentie om die aandelen en dus concurrentie tussen jouw agents en de andere agents in het handelsproces. De agents vertonen nu competitief gedrag. Ander voorbeeld: stel je voor dat er kunstmatige intelligentie in je koelkast zit. Zodra bij jou thuis de boter op is, probeert de koelkast-agent een zo goed mogelijke deal te sluiten. Hij probeert dan dus de beste boter te kopen voor de laagste prijs. De verkoop-agents van de winkels die boter verkopen, hebben een tegengesteld belang. Zij proberen een zo hoog mogelijke prijs te krijgen voor een pak boter. De verkoop-agents zijn in dit geval dus competitief. Toch moet er tot een overeenkomst gekomen worden. De agents gaan hierover met elkaar in onderhandeling.
Een mix van concurrentie en samenwerking is ook mogelijk. Onderzoek in die richting in robotica vindt onder andere plaats bij robotvoetbal.

## Omgeving

Een agent bevindt zich in een *omgeving*. In het Engels spreken we van een *environment*. In deze omgeving kan een agent acties uitvoeren. Het hangt af van de aard van de agent in welke omgeving deze kan handelen. Je hebt bijvoorbeeld omgevingen die puur softwarematig zijn. Een game zoals World of Warcraft is hier een voorbeeld van. De agents kunnen hierbinnen van alles doen, zoals een gevecht starten. De zelfrijdende auto is een agent in de echte wereld die uit andere agents bestaat. In figuur 1 zie je een schematische weergave van een agent en de omgeving. Binnen multi-agent systemen kunnen we de volgende omgevingen onderscheiden:

- Virtuele omgevingen. In bijvoorbeeld games, simulaties en online handel kom je die tegen.
- Discrete omgevingen. De agents kunnen zich in een eindig aantal posities bevinden en ook slecht een eindig aantal handelingen verrichten. Een schaakspel is een dergelijke omgeving.
- Continue omgevingen. De verkeerssituatie is een dergelijke omgeving. Een agent kan overal in de ruimte plaatsnemen en zijn eigen positie verandert ook geleidelijk.

## Agents

Het is nog wel even nuttig om stil te staan bij de verschillende typen agents. In een omgeving is eigenlijk alles waarop een agent moet reageren zelf weer een agent. Dus in de verkeerssituatie is niet alleen de zelfrijdende auto een agent, maar ook de wandelaar, de fietser, de bestuurder van een auto. Zelfs de verkeersheuvels en verkeersborden worden als agents beschouwd. Dit leidt tot de volgende grove indeling voor agents:

- Passieve agents of "agent zonder doel" (verkeersborden, een aandeel of in een spel een wapen of schat );
- Actieve agents met een simpel doel (robot in een distributie magazijn);
- Intelligente agents (zelfrijdende auto, mens, dier).

## Agent in de omgeving

Actieve en intelligente agents nemen hun omgeving in meer of minder detail waar. Afhankelijk van de taak en training reageert een agent. Iedere actie van een agent verandert de toestand van die agent, maar tegelijkertijd ook de omgeving van zichzelf en andere agents.  Bijvoorbeeld één  van de doelen van een bestuurder van een auto is ‘bots nergens tegenaan’. Als er een obstakel in beeld komt waar de auto niet omheen kan zal de auto tot stilstand moeten worden gebracht. De bestuurder remt. De toestand van de agent wordt anders. Positie en snelheid veranderen. Een agent in het achterop komend verkeer neemt hopelijk die verandering waar, want de omgeving voor deze agent is ook veranderd. Kortom een multi-agentsysteem is een samenspel van waarnemingen, acties en reacties.

::::{admonition} 🛠️**Vragen**

Denk eens na over het volgende probleem. Beantwoord daarna de vragen.

In een zelfrijdende auto zit een man. Deze man is in bezit van een agent van een applicatie die zelfrijden van een auto mogelijk maakt. De auto rijdt ongestoord met een redelijke snelheid als er plots een vrouw met een kinderwagen oversteekt. De agent heeft niet genoeg tijd om te remmen om de oversteker te redden. Rechts van de weg staat een boom. De agent moet heel snel handelen; er is geen tijd om te vragen wat de inzittende man wil. De agent kan twee acties uitvoeren:

**Actie A: Remmen**

Als de agent remt, dan komt de auto tot stilstand en dan is de inzittende man gered. De vrouw met de kinderwagen overleeft dit niet.

**Actie B: Tegen de boom aanrijden**

Als de agent naar rechts stuurt en tegen de boom aanrijdt, dan is de vrouw met de kinderwagen gered. De inzittende man overleeft dit niet.

1. Wat moet een kunstmatige intelligente agent volgens jou leren, actie A of actie B?
2. Stel dat we de rollen omdraaien. In de auto zit nu een vrouw met een kind en een man steekt plotseling over. Verandert dit jouw vorige antwoord? Waarom wel/niet?
3. Stel er komen vliegende drones die patiënten van geneesmiddelen voorzien. Welke agents zijn er zeker in de omgeving van de drone te vinden. Geef aan tot welke type de agents behoren.
4. Geef voorbeelden bij de drie verschillende omgevingen waarin een agent zich kan bevinden.

:::{dropdown} Antwoorden
1. Dit is een bekend ethisch dilemma waar agents mee te maken kunnen krijgen. Hier is eigenlijk geen goed of fout antwoord op te geven. Het doel van deze vraag is om jou te laten inzien dat het soms niet eenvoudig is om de juiste actie te bepalen. Een mogelijk antwoord is actie B, omdat daar meer mensenlevens mee bespaard worden. Je kunt ook actie A beargumenteren, omdat de agent in dienst staat van de man in de auto.
2. Net als bij de vorige vraag is deze niet goed of fout te beantwoorden, zolang je een goede onderbouwing geeft.
3. Vergelijkbare drones (Intelligente agent),
Patiënt (Intelligente agent),
Huizen (Passieve agents),
Apotheek (Intelligente agent),
...
4. Zie de tekst.
:::
::::

## Kenmerken van een multi-agentsysteem

Er zijn veel verschillende kenmerken van multi-agentsystemen. We hebben tot dusver al een aantal kenmerken genoemd. We zetten de belangrijkste kenmerken van een multi-agentsysteem hier op een rijtje:

**De organisatie binnen een multi-agentsysteem is *decentraal***

Een belangrijk kenmerk van een multi-agentsysteem is dat het decentraal is. Dat houdt in dat er niet zoiets bestaat als een coördinator of centraal bestuur. De agents hebben tot op zekere hoogte autonomie, wat betekent dat ze zelf bepalen wat en wanneer ze iets doen om hun doelen te behalen. Denk weer even terug aan de zelfrijdende auto. Elke auto gaat zijn eigen weg. Er is geen centraal beheer dat alle zelfrijdende auto’s bestuurt.

**Agents functioneren binnen een *omgeving***

Een agent moet zich in een omgeving bevinden. Binnen zo’n omgeving moet een agent het volgende kunnen doen:

- Observaties van de omgeving. De agent moet een deel van de omgeving kunnen waarnemen. In het geval van een zelfrijdende auto of andersoortige robot gebeurt dat door middel van sensoren en camera’s.
- Acties binnen de omgeving. De agent moet invloed kunnen uitoefenen op een omgeving door middel van acties. Bij een zelfrijdende auto of andersoortige robot zou je spreken van *actuatoren*. Een actuator is het tegengestelde van een sensor: er komt geen informatie binnen, maar er wordt iets naar buiten gebracht. Remmen, sturen of toeteren zouden acties kunnen zijn van een zelfrijdende auto.

**Agents doen *aannames***

Agents nemen altijd maar *een deel van hun omgeving waar*. Dit is niet omdat deze agents niet alles mógen zien, maar eerder omdat de omgeving voor een agent te complex is om volledig te kunnen overzien. Agents zijn dus niet alwetend over hun omgeving, maar hebben kennis over die omgeving die ook wel aannames over de omgeving worden genoemd. Een aanname is dus iets wat een agent eerder heeft waargenomen en geleerd, maar wat niet per se hoeft te kloppen. Bijvoorbeeld, een ‘stofzuiger-agent’ heeft met zijn sensor een plantenbak waargenomen en legt vast dat er op die locatie een plantenbak staat. Als iemand vervolgens de plantenbak weghaalt en de agent heeft deze actie niet waargenomen, dan heeft de agent nog de, inmiddels onjuiste, kennis dat de plantenbak er nog staat. Pas als de agent weer opnieuw op de oude plek van de plantenbak komt, neemt deze waar dat de aanname niet meer klopt en wordt deze aangepast.

::::{admonition} Vragen

1. Stel dat je een agent voor een zelfrijdende auto hebt. Wat zou dan een **omgeving** kunnen zijn? Geef ook een voorbeeld van een mogelijke **observatie** en een **actie**.
2. Noem 3 kenmerken van een multi-agentsysteem.
3. Bekijk de video hieronder: 
Er zijn meerdere robots te zien, maar de rijdende robotkast is het meest in beeld. Waaruit bestaat de omgeving van deze robot? Wat is de hoofdtaak van de robot en welke subdoelen zijn nodig voor goed functioneren.

:::{dropdown} Antwoorden
- Antwoorden
    1. Een omgeving is de snelweg met alleen andere auto's. Een andere omgeving is een smalle gracht in Amsterdam met eenrichtingsverkeer voor auto's en fietsers en wandelaars op de rijbaan. Op de snelweg observeert de auto met de **gps** dat de afslag van het doel naderbij komt. De auto **stuurt** naar de afrit.
    2. De organisatie binnen een multi-agentsysteem is *decentraal.*
    Agents functioneren binnen een *omgeving.*
    Agents doen *aannames.*
    3. De robot bevindt zich in het magazijn en heeft behalve de inrichting van magazijn ook nog de andere robotkasten als omgeving.
        * Het hoofddoel is het rijden naar de inpakafdeling en weer terug naar een lege plek na aflevering.
        * De subdoelen zijn: niet botsen met andere robots en netjes parkeren.
:::

::::

# Agent-based modellen in multi-agentsystemen

Hoewel agent-based modellering niet het zelfde is als een multi-agentsysteem worden er wel elementen uit het onderzoek in agent-based modellering ingezet in multi-agentsystemen om doelen van de applicaties te kunnen bereiken. We bekijken een competitief en een samenwerkend model.

## Competitief: Speltheorie

Agents zijn onafhankelijk en moeten dus zelf beslissingen nemen zonder dat er mensen bij betrokken zijn. In een multi-agentsysteem moet elke agent ook rekening houden met de acties van anderen en de consequenties daarvan. Soms, maar niet altijd, zijn de doelen van agents onderling tegenstrijdig of wel competitief. Als dat het geval is, dan moet een agent slimme keuzes maken. Daarbij kan [**speltheorie**](https://towardsdatascience.com/game-theory-in-artificial-intelligence-57a7937e1b88) toegepast worden.



Bij speltheorie worden situaties vertaald naar punten die deelnemers kunnen verdienen. Net zoals bij een spelletje is het doel van een agent om zo veel mogelijk punten te scoren. Een agent kan een bepaalde actie doen, waardoor een bepaalde situatie ontstaat. Voor elke situatie die kan ontstaan, verdienen de agents die meedoen meer of minder punten.

Speltheorie wordt vaak geïllustreerd door middel van een matrix. In de matrix staan de acties van alle spelers tegenover elkaar. Hieronder zie je een voorbeeld van hoe je het spelletje steen-papier-schaar in een matrix zet:

Zoals je ziet, verdienen de spelers punten als ze in een bepaalde situatie terechtkomen. In dit geval heeft elke speler drie opties om te spelen: steen, papier of schaar. De score wordt bepaald nadat beide spelers hun keuze hebben gemaakt. In dit voorbeeld heeft elke speler maar een paar opties. Er zijn echter ook situaties waarin je per speler tientallen opties hebt of nog wel meer. In het steen papier schaar spel is de puntenverdeling in balans. Er is eigenlijk geen beste keus te maken om te winnen. Dit is ook niet altijd het geval.

Neem bijvoorbeeld een schaakcomputer. Elke mogelijke zet van beide spelers is een optie en zou je in zo’n matrix kunnen zetten. Daarnaast hebben de stukken niet een gelijk waarde, een pion die een koningin slaat verdient meer punten dan andersom. Een schaakcomputer gebruikt soortgelijke matrices, maar rekent zelfs de zetten nog door: er worden dan heel veel van zulke matrices berekend. De zet met de meest gunstige uitkomst wordt dan gekozen. Speltheorie leent zich goed voor zulk soort games.

### Prisoners dilemma

De volgende opdracht is klassikaal. Voer deze uit voordat je doorgaat met de theorie.

:::{admonition} 🛠️ Groepsopdracht

**Benodigdheden**

Per persoon een pen en een aantal papiertjes.

**Voorbereiding**

Verdeel de klas in groepjes van minimaal 2 personen. Het beste is als er groepjes zijn met verschillende groottes, variërend van 2 tot 6 personen.

**Werking**

Elk groepje speelt afzonderlijk 10 beurten. Aan het begin van elke beurt schrijft iedereen een ‘1’ of een ‘0’ op een briefje, zonder dat de anderen het zien. Als iedereen een getal heeft opgeschreven, dan laat iedereen tegelijk zijn/haar getal binnen de groep zien. Afhankelijk van de getallen die zijn opgeschreven, krijgen alle deelnemers van de groep punten. Iedereen heeft als doel om als *individu* de meeste punten van de *klas* te halen.

De regels voor het tellen van de punten zijn als volgt:

| Situatie | Puntentelling |
| --- | --- |
| Alle groepsleden hebben 1 opgeschreven | Elk groepslid krijgt 3 punten |
| Alle groepsleden hebben 0 opgeschreven | Elk groepslid krijgt 1 punt |
| Sommige groepsleden hebben 1 andere hebben 0 opgeschreven | De groepsleden met een 1 krijgen 0 punten; de groepsleden met een 0 krijgen 5 punten |

:::

::::{admonition} Vragen

1. Wie heeft er gewonnen? Zat deze persoon in een klein groepje of een grotere?
2. Heeft de winnaar vaker `1` of `0` opgeschreven?
3. Werd er in veel groepjes overlegd?
4. Denk je dat de uitslag anders was geweest met of zonder overleg in de groepjes?
5. Zou je jouw eigen strategie aanpassen nu je ervaring hebt met dit spel?
:::{dropdown} Antwoorden
1. Hoe groter de groep, hoe groter de kans dat er iemand ‘0’ opschrijft. Dan is een klein groepje dus succesvoller. Maar de grootste kans om te winnen heb je tussen mensen die je goed kunt vertrouwen. Je vrienden bijvoorbeeld.
2. Waarschijnlijk heeft de winnaar meestal ‘1’ opgeschreven om vertrouwen te winnen. Misschien in de laatste beurten schreef hij/zij ‘0’.
3. Het is aantrekkelijk om hierbij te overleggen en een strategie af te spreken. Het probleem is alleen dat je niet weet of je de anderen kunt vertrouwen.
4. Het zal misschien niet eens veel uitmaken. Iedereen heeft een individueel doel en de medespelers zijn tegenstanders. Je hebt dan dus een motief om te liegen over de strategie die je afspreekt.
5. Als je met dezelfde mensen speelt, is dat misschien wel handig. Ze hebben immers de strategie die je eerder speelde al gezien.
:::
::::

Je hebt zojuist kennisgemaakt met het *prisoners dilemma*. Dit is een probleemstelling waar een agent mee te maken kan krijgen. Het probleem bij het prisoners dilemma is de keuze tussen de winst van de groep en de winst van het individu. Als alle partijen in een prisoners dilemma voor de groep kiezen (in de opdracht was dat ‘1’ opschrijven) dan wordt iedereen daar beter van. Helaas weet je niet of je iedereen kunt vertrouwen.

Het prisoners dilemma wordt vaak uitgelegd met het voorbeeld van twee verdachten bij de politie. Alice en Bob zijn opgepakt voor een overval en worden allebei afzonderlijk verhoord. De verhoorder vertelt beide verdachten hetzelfde: “Als jij meewerkt en getuigt, dan ga je vrij en zit je partner een straf van 10 jaar uit. Maar als jullie allebei tegen elkaar getuigen, dan zitten jullie allebei vast voor 5 jaar.” Alice en Bob weten dat als ze beiden weigeren te getuigen, ze beiden slechts een straf van 1 jaar krijgen. Wat is nu de meest logische optie: getuigen of weigeren? Je kunt een prisoners dilemma in een matrix vatten om het overzichtelijk te maken:

### Dominante strategie

De matrix hierboven helpt om het probleem inzichtelijker te maken en te bepalen wat de meest logische keus is. Stel dat je in de schoenen van Alice staat. Als Bob kiest om te getuigen, dan krijgt Alice 5 jaar als ze zelf ook getuigt en 10 jaar als ze weigert; getuigen is dan de betere keus. Als Bob er voor kiest om te weigeren, dan krijgt Alice 0 jaar als ze getuigt en 1 jaar als ze weigert; ook hier is getuigen de betere keus. In dit voorbeeld is getuigen een zogenaamde *dominante strategie*. In dit geval geldt voor Alice dat de strategie om te getuigen de strategie om te weigeren *sterk domineert*. Dat is zo omdat alle uitkomsten voor Alice bij getuigen beter zijn dan weigeren, ongeacht welke strategie Bob kiest.

Voor Bob geldt trouwens hetzelfde: ook zijn dominante strategie is om te getuigen. Waarschijnlijk zullen Bob en Alice beiden voor hun dominante strategie kiezen en getuigen. Het is namelijk voor geen van beiden aantrekkelijk om van deze strategie af te wijken: ze krijgen dan meer straf. We spreken hier van een *dominante strategie evenwicht*, omdat alle partijen in hun dominante strategie blijven hangen. Een andere naam hiervoor die vaak gebruikt wordt is *Nash evenwicht* (naar John Nash, de bedenker hiervan).

::::{admonition} 🛠️ Vragen

1. Stel een matrix op voor de groepsopdracht aan het begin van deze paragraaf.
2. Wat is de dominante strategie?
3. Leg uit of de dominante strategie sterk domineert.
4. Is er ook sprake van Nash evenwicht?
5. Zoek zelf een voorbeeld van het prisoners dilemma in het dagelijks leven.

:::{dropdown} Antwoorden
1.
2. Stel dat alle andere groepsleden `0` opschrijven. Dan is het gunstiger voor jou om `0` op te schrijven. Stel dat alle andere groepsleden `1` opschrijven. Dan is het nog steeds gunstiger voor jou om `0` op te schrijven. De dominante strategie is dus om `0` op te schrijven.
3. Ja, de strategie om `0` op te schrijven is een sterk dominante strategie. De uitkomst is altijd beter wanneer je `0` opschrijft. Voor het individu is dit de beste strategie, maar voor de groep als geheel niet. De groep als geheel kan de meeste punten verdienen door altijd `1` op te schrijven.
4. Er is hier sprake van een Nash evenwicht. Omdat voor alle groepsleden geldt dat het ongunstig is om van zijn/haar dominante strategie af te wijken. Iedereen blijft dus bij dezelfde strategie.
5. Een voorbeeld van het prisoners dilemma is het gebruik van doping in de sportwereld. In sommige sporten wordt er veel doping gebruikt. Als alle andere sporters ook doping gebruiken, dan ben jij in het nadeel door dat niet te doen. Als jij als enige doping gebruikt en de rest doet dat niet, dan ben jij in het voordeel.
:::
::::

Je kunt speltheorie niet alleen bij games gebruiken, maar ook in het echte leven. Als een zelfrijdende auto is voorbereid voor deelname in het verkeer moet deze voorbereid zijn op acties van andere agents, waaronder andere zelfrijdende auto's. Laten we ons voorstellen dat we proberen de verkeersstroom in een stad te verbeteren met behulp van een groep AI-aangedreven zelfrijdende auto's. Op zichzelf kan elk van de auto's perfect communiceren met de externe omgeving, maar het kan ingewikkelder worden als we de auto's als een groep willen laten denken. Een auto kan bijvoorbeeld in conflict komen met een andere omdat het voor beiden het handigst is om een bepaalde route te volgen. Speltheorie kan dan deel uitmaken van het leerproces om de AI verstandige keuzes uit te laten voeren.

## Samenwerkend: Zwermintelligentie

Als een systeem bestaat uit een groot aantal eenvoudige eenheden die gezamenlijk een complexe taak kunnen uitvoeren, dan is er sprake van *zwermintelligentie*. Zoals de meeste uitvindingen van de mens, is ook de zwermintelligentie gebaseerd op een verschijnsel uit de natuur. Denk aan een zwerm spreeuwen die samen een golf aan bewegingen maken, een kolonne mieren op weg naar voedsel, trekkende gnoes in Afrika en keizerpinguïns op Antarctica.


Zwermintelligentie in AI is een bijzondere vorm van een multi-agentsysteem: het voldoet aan alle drie de genoemde kenmerken van de vorige paragraaf. Je moet zwermintelligentie zien als een subgroep van de bredere groep van multi-agentsystemen. Kenmerkend voor een taak voor zwermintelligentie is dat de agents individueel niet complex hoeven te zijn en de taak vrij eenvoudig is. Het resulterende samenwerkende gedrag lijkt dan intelligent.



Kenmerken van een zwermintelligentie:

- Er zijn veel agents.
- De agents van de zwerm reageren sterk op elkaar of werken samen.
- Het gedrag van de individuele agents voor de zwermtaak is eenvoudig.
- Het gedrag van de zwerm is complex.

Het conflict dat zelfrijdende auto's in de speltheorie sectie hebben opgeworpen zou wel eens door het inzetten van [zwermintelligentie](https://www.bosch-presse.de/pressportal/de/en/swarm-intelligence-for-automated-driving-231431.html) kunnen worden opgelost. Hoewel de agents een conflicterend doel hebben namelijk dezelfde koers, kan er bijvoorbeeld voor worden gekozen om dicht achter elkaar aan te rijden om zo energie uit te sparen. Voorwaarde is dan natuurlijk wel dat de auto's met elkaar kunnen communiceren. Het 5G netwerk is deels ontworpen met zulke doelen in het vooruitzicht.

::::{admonition} 🛠️ Opdracht

In de applet hieronder (open de volledige applet door op de onderstaande link te klikken) kun je experimenteren met attractie en afstoting om het zwermgedrag te veranderen. Wil je hier meer over weten ga dan naar de bron: [Job Talle](http://jobtalle.com/swarm_behaviour.html). De schuifjes hebben de volgende betekenis.

- *Agent snelheid (speed)* bepaalt de minimum snelheid van een agent; een agent die niet wordt beïnvloed door de omgeving zal met deze snelheid bewegen.
- De zones van *Afstoting (repulsion)*, *uitlijning (alignment)* en *aantrekkingskracht (attraction)* bepalen de stralen van cirkelsegmenten rond de agent waarin deze omgevingsinvloeden werken. Alle invloeden tellen bij elkaar op, resulterend in het getoonde gedrag.
- Het cirkelsegment wordt bepaald door *de kijkhoek (attraction angle)* van de agenten in graden.
- De krachten (strength / force) bepalen de grootte van de invloed. Bijvoorbeeld, als een agent een andere agent in zijn afstotingszone heeft dan zal de snelheid waarmee deze agent zich verwijdert worden bepaalt door de grootte van de kracht *Repulsion force*. Als er meer agenten in de afstotingszonde zijn dan wordt de afstotingskracht evenredig groter. Dus hoe groter het aantal agenten hoe groter de snelheid waarmee de agent weg gaat.
- *Zwaartekracht (Gravitation force)* bepaalt de kracht waarmee agents naar het midden van het scherm worden getrokken. Deze kracht zorgt er onder meer voor dat en groep agenten als één geheel kunnen draaien.
- Voor de wiskundigen onder jullie, klap deze sectie uit.
:::{dropdown} formules    
Per stap wordt de snelheid van een agent volgens de volgende formule veranderd:
    
$$
\vec{v}_{volgende} = |\vec{v}| * s + \sum_{n=1}^{rc} |\vec{r_n}| * f_r + \sum_{n=1}^{ac} |\vec{a_n}| * f_a + \sum_{n=1}^{tc} |\vec{t_n}| * f_t
$$
    
Hierin is $\vec{v}$ de snelheid, $s$ de snelheid van de agent, $rc$, $ac$ en $tc$ zijn de aantallen andere agenten in de afstotings-, uitlijnings en aantrekkingskracht-zone van de agent. $\vec{r_x}$, $\vec{a_x}$ en $\vec{t_x}$ zijn de groottes van de afstotings-, uitlijnings en aantrekkingskracht-vectoren van agent $x$, als laatste zin $f_r$, $f_a$ en $f_t$ de krachten ingesteld voor afstoting, uitlijning en aantrekkingskracht. De zwaartekracht is nog niet meegenomen in deze formule.
:::    

Onderzoeksvragen:

1. Zet alle krachten op nul en druk op scatter, wat neem je waar?

:::{dropdown} antwoord        
Er is geen groepsvorming.
:::
        
2. Onderzoek het effect van alleen de uitlijningskracht door de zone en de kracht maximaal te kiezen. Wat neem je waar?
:::{dropdown} antwoord        
Alle agents gaan in de zelfde richting bewegen.
:::        
3. Breidt je onderzoek naar de invloed van afzonderlijke krachten uit. Wat neem je waar?
:::{dropdown} antwoord     
Zwaartekracht: Alle agents bewegen zich naar het midden. Ze beïnvloeden elkaar echter niet.
        
Afstotingskracht: Als de snelheid van de agent hoog is zie je niet veel veel verschil met totaal geen krachten, er zijn wel minder "botsingen". Bij lage snelheden zie je dat iedere agent min of meer een eigen gebiedje krijgt.
        
Aantrekkingskracht: Als de hoek van aantrekkingskracht 0 is is de situatie gelijk aan geen krachten. Met een hoek van 360 graden zie je dat de agents clusteren net als bij zwaartekracht, maar er kunnen meerdere clusters zijn en de cluster zit niet midden in het scherm.e agents beïnvloeden zich hier het meest.
:::
        
4. Probeer eens situaties te maken waar nauwelijks groepsvorming is en situaties waar de agents zowat aan elkaar vast zitten.
5. Vind je na dit experiment dat de zwerm intelligent is of vind je dat het alleen maar zo lijkt? Geef aan waarom je jouw conclusie trekt en vergelijk jouw conclusie met een andere leerling.
::::