# Machine learning

In de [introductie](https://www.notion.so/3-1-Introductie-b49a35ee8d8b45bba29636e026abc2fa?pvs=21) van dit hoofdstuk heb je gezien dat er onderscheid werd gemaakt tussen niet lerende en lerende AI. Lerende AI noemen we **machine learning**. Machine learning vindt plaats aan de hand van data. Het leerproces levert een algoritme dat een **agent** (vertegenwoordiger van leerproces) gebruikt om te reageren op vragen van de gebruiker. Een gebruiker hoeft daarin niet een persoon te zijn, daarover later meer in de sectie  [multi-agentsystemen](https://www.notion.so/3-7-Multi-agentsystemen-0fb0126dccb2403d842753d2f513b991?pvs=21). Machine learning wordt weer onderverdeeld in een groep waar de relatie tussen data en de uitvoer van het geleerde algoritme van de agent vast ligt en een groep waarin de relatie tussen de data en de uitvoer van het geleerde algoritme onbekend is. De machine learning techniek die in de laatste situatie wordt hoort bij neurale netwerken en wordt deep learning genoemd.

Machine learning (of **machinaal leren** in het Nederlands)  leert dus van data. De technieken binnen machine learning zorgen ervoor dat een systeem steeds beter wordt in een taak of zich steeds beter aanpast aan zijn omgeving. Mensen vinden deze vorm van kunstmatige intelligentie vaak fascinerend, omdat het lijkt alsof een systeem als vanzelf slimmer wordt. Het kunnen leren wordt dan ook vaak gekoppeld aan intelligentie; een hond die goed leert, noemen we ook slim.

Er zijn mooie voorbeelden op het internet te vinden van toepassingen van machine learning. Vaak gaat het dan om een combinatie van meerdere machine learning-technieken. In deze filmpjes is een computerprogramma getraind om Super Mario te spelen. Het is opvallend hoe goed de computer uiteindelijk geworden is.

:::::{grid} 1 1 2 2

::::{grid-item}
:::{image} figs/technieken-image3.png
:width: 350
:::
::::

::::{grid-item}
:::{image} figs/technieken-image4.png
:width: 350
:::
::::
:::::

::::{admonition} 🛠️ Vragen

1. Denk je dat de agent (Super Mario) bijleert tijdens het spelen van een level, of steeds aan het einde?
2. Stel dat je de agent laat stoppen met leren en hem neemt zoals hij is aan het einde van het filmpje. Denk je dat hij ook goed zou kunnen presteren in een ander level?

:::{dropdown} Antwoorden
1. Waarschijnlijk leert de agent steeds aan het einde. Als Mario afgaat, dan is dat een signaal aan de computer om de volgende keer net iets anders te spelen.
2. Bij de meeste games worden de levels steeds moeilijker en verschijnen er nieuwe uitdagingen. Als de agent alleen maar getraind is in dit level, zal hij waarschijnlijk niet zo ver komen.
:::

::::

# Online en offline leren

Je kunt machine learning-algoritmen verdelen in twee groepen, namelijk in *online learning-* en *offline learning***-**algoritmen. Deze groepen hebben niets te maken met verbindingen met het internet, maar de termen hebben betrekking op het moment waarop een algoritme aan het leren is. Online learning is leren ‘on the job’.  Hierbij leert het algoritme terwijl het in productie draait. [Spraakherkenning](https://blogs.fireflies.ai/how-does-voice-recognition-work/) is hier een voorbeeld van. De software kan per persoon leren welke uitspraak van deze persoon bij welk woord hoort. Bij offline learning wordt het algoritme van tevoren getraind, waarna het in productie wordt genomen. Een postsorteerrobot is daar een voorbeeld van.  De robot heeft een algoritme dat, op basis van heel veel voorbeelden, is ontstaan door training met het offline-learning algoritme. Eenmaal in de hal van de postverwerking geplaatst, zal deze robot niet meer bijleren.

## Categorieën machine learning

Er zijn verschillende manieren om een computerprogramma iets aan te leren, net zoals er verschillende manieren zijn om mensen iets aan te leren. Denk bijvoorbeeld aan boekjes voor kleine kinderen met eenvoudige woorden en bijbehorende plaatjes (boom, huis, kat, etc.). Het kind wordt hierbij als het ware aan de hand genomen tijdens het leren.

Een andere, minder behulpzame manier om iets aan te leren, is door simpelweg in het diepe te worden gegooid. Dit gebeurt bijvoorbeeld als je zonder voorbereiding naar het buitenland gaat en langzaam de taal ‘vanzelf’ leert te begrijpen.

Weer een andere manier om te leren, is door je eigen gedrag te toetsen en daardoor te verbeteren. Onbewust deed je dat als klein kind toen je met vallen en opstaan leerde lopen. Als je nu bijvoorbeeld voor een sport traint of een muziek instrument leert bespelen dan doe je dat waarschijnlijk bewuster. Je probeert met telkens net iets andere handelwijzen en door zelf je resultaten te observeren (in de momenten zonder trainer) tot de beste handelwijze te komen.

Deze manieren van leren hierboven genoemd worden ook binnen machine learning gebruikt. We onderscheiden de volgende drie basisvormen:

1. **supervised learning** (begeleid leren);
2. **unsupervised learning** (onbegeleid leren);
3. **reinforcement learning** (versterkend leren).

Zoals gezegd vormen deze categorieën de basis voor machine learning. Dat wil zeggen dat er nog meer zijn. Zo kom je bijvoorbeeld ook tussenvormen tegen. We behandelen hier echter alleen deze drie basiscategorieën.

## Supervised learning

Supervised learning lijkt op het leren met het kleuterboekje: een agent krijgt voorbeelden met betekenissen te zien en wordt aan de hand van deze voorbeelden getraind om zelf conclusies te trekken. Deze vorm van leren wordt toegepast in het trainen van [neurale netwerken](https://www.notion.so/a0cfa2a90fc244f98f28bf75a7dd10d9?pvs=21).

Stel dat je een applicatie wil gebruiken om afbeeldingen te herkennen, dan moet deze eerst leren van een reeks met afbeeldingen met de bijbehorende woorden. De agent van de applicatie heeft als doel om een willekeurige afbeelding te voorzien van een etiket: om de gegeven afbeelding in een bepaalde geleerde categorie te plaatsen. Het herkennen van beeldmateriaal, zoals handschriftherkenning, is hiervan een voorbeeld. Bij deze manier van machine learning zijn er drie fases: de *training-*, de *validatie-* en de *testfase*.

**Fase 1: training**

De trainingfase is de eerste van de drie. Hier wordt de agent voorzien van voorbeelden om mee te trainen, de zogenaamde **trainingset**. De agent zal zich herhaaldelijk over de trainingsset buigen, voordat er naar de volgende fase wordt overgegaan.

**Fase 2: validatie**

De validatiefase volgt op de trainingfase. In deze fase wordt de huidige werking van de getrainde agent gevalideerd; dat wil zeggen dat gecontroleerd wordt hoe goed deze getraind is. Hier wordt de zogenaamde *validatieset* voor gebruikt. Dit is een vergelijkbare reeks voorbeelden als bij de trainingset, maar ze zijn nooit hetzelfde. Als de agent deze validatieset goed verwerkt, dan wordt overgegaan op de volgende fase. Als de uitkomsten echter niet acceptabel zijn, dan moeten het programma en/of de trainingset worden aangepast en wordt teruggegaan naar de trainingfase.

**Fase 3: testen**

Ten slotte is er de testfase. Deze naam is misschien misleidend, want in deze fase wordt de agent echt in gebruik genomen. Deze fase heeft dus niets te maken met software testen! Bij deze daadwerkelijke toepassing van de getrainde agent, noemen we de input die het programma krijgt, de *testset*.

Omdat bij een zuiver supervised learning-algoritme altijd alleen geleerd wordt tijdens de trainingfase (en niet in de testfase), spreken we bij deze categorie van offline learning.

### Overfitting

Het trainen van een applicatie doe je om de agent in de praktijk te kunnen gebruiken met inputs die je nog niet weet. Bijvoorbeeld, als je een agent bouwt die handgeschreven tekst moet kunnen herkennen, dan kun je niet alle handschriften ter wereld in de trainingsfase stoppen. Bij het trainen van een agent is er een gevaar dat je de agent te goed leert werken met de trainingset. Je noemt dit *overfitting*. De validatie fase is onder andere nodig om deze overfitting te voorkomen.

Aan het begin van dit hoofdstuk heb je een filmpje van Super Mario bekeken. Omdat Super Mario steeds hetzelfde level speelt, is hier sprake van overfitting. De agent zal in een ander level waarschijnlijk heel slecht presteren.

## Unsupervised learning

Bij unsupervised learning wordt de agent aan zijn lot overgelaten. Er wordt hem van tevoren niets ingefluisterd en er worden geen voorbeelden gegeven. Deze manier van leren heeft heel andere doeleinden dan bij supervised learning. Je kunt bijvoorbeeld geen handschriftherkenning met unsupervised learning voor elkaar krijgen; de agent heeft namelijk nooit etiketten – in dit geval de letters van het alfabet – gekregen.

### Clustering en Associatie analyse

Cluster en associatie analyse die vallen beide onder unsupervised machine learning. Bijvoorbeeld, bij clusteren wordt de data verdeeld groepjes, in clusters. De agent die aan het leren is, kan deze indelingen maken zonder de betekenis van deze clusters te weten. Als je dus bijvoorbeeld unsupervised learning toepast op handgeschreven letters, dan deelt de agent misschien de ‘u’ en de ‘v’ in een cluster (op basis van hun vormen) en de ‘i’ en de ‘j’ in een ander cluster, zonder te weten dat dit letters van ons alfabet zijn. Bij associatie analyse bepaalt de data welke onderdelen in de dataset meer met elkaar geassocieerd zijn ofwel welke onderdelen meer verband met elkaar houden. Er is van te voren geen oordeel over welke verband er moet zijn. In de secties [cluster analyse](https://www.notion.so/7cf0b1c90c364061bc52aabe1afd4fa7?pvs=21) en [associatie analyse](https://www.notion.so/c9bc318c726243a480de86b38c390904?pvs=21) bekijken we unsupervised leren in detail.

## Reinforcement learning

De laatste categorie machine learning die we behandelen, is reinforcement learning. Deze vorm van leren is een speciaal geval van begeleid leren. De applicatie is zijn eigen trainer. Bij deze categorie van machine learning zoekt de agent naar oplossingen voor een probleem en bepaalt de agent na iedere poging zelf hoe goed hij gepresteerd heeft. Denk aan een kleine muis die door een doolhof rent. Als hij bij een T-splitsing naar links draait, krijgt hij een stukje kaas; als hij naar rechts draait, krijgt hij een kleine elektrische schok (maak je geen zorgen, dit is maar een doe-alsof-muis). Vermoedelijk zal de muis na verloop van tijd leren om naar links te draaien. Zijn neurale netwerk neemt een beslissing met een uitkomst (draai naar links of rechts) en observeert zijn omgeving (lekker of au). Je zou dus kunnen zeggen dat bij reinforcement learning goed gedrag beloond wordt en slecht gedrag bestraft. Dit moment van belonen vindt altijd achteraf plaats, dus nadat de agent zelf heeft gehandeld in een bepaalde situatie. De beloning zelf heet het **reinforcement signal**. Het Super Mario-filmpje is een voorbeeld van reinforcement learning.

### Kenmerken van toepassingen van reinforcement learning

Om reinforcement learning toe te passen op een probleem, moet het probleem zich wel lenen voor deze categorie van machine learning. Er zijn meerdere kenmerken waaraan een probleem kan voldoen, waaruit blijkt in hoeverre dit door een reinforcement learning-algoritme kan worden opgepakt. We noemen er een aantal:

**De oplossingen zijn voldoende meetbaar**

Voor een reinforcement signal is het nodig dat deze afgeleid kan worden van de door het programma bedachte oplossingen. De oplossingen moeten dus meetbaar zijn, zodat ze kunnen worden vertaald naar dit reinforcement signal.

**De omgeving is voldoende *deterministisch***

Een omgeving is deterministisch als je precies kunt bepalen hoe de omgeving eruit ziet na een actie. Een schaakbord is bijvoorbeeld deterministisch (want je weet precies hoe de stukken staan na elke zet). Als een omgeving niet deterministisch is (b.v. het resultaat van een worp met een dobbelsteen), dan weet je dus niet of de acties van het computerprogramma hebben geleid tot een bepaalde oplossing en dan kun je dus ook geen reinforcement signaal toekennen. Is er slechts kleine variatie in de uitkomst van een experiment bij een bepaalde beginsituatie dan kan het systeem nog voldoende deterministisch zijn voor een succesvol leerproces.

**Er is genoeg ruimte om te leren**

Reinforcement learning is leren met vallen en opstaan. Sommige problemen lenen zich hier niet voor, omdat er geen ruimte is voor fouten. Reinforcement learning is bijvoorbeeld niet geschikt om een apparaat slim genoeg te maken om een hartfilmpje te leren monitoren: fouten zijn te cruciaal.

::::{admonition} 🛠️ Vragen

Speel even met onderstaande [vogelapplicatie](https://experiments.withgoogle.com/ai/bird-sounds/view/). Let op: zet je geluid niet te hard! Beantwoord daarna de volgende vragen.




1. Wat is hier waarschijnlijk gebruikt om de kunstmatige intelligentie te trainen: supervised, unsupervised of reinforcement learning? Leg uit waarom je dit denkt.
2. In het [filmpje](https://experiments.withgoogle.com/ai/bird-sounds/view/) dat erbij hoort leggen de makers uit wat ze hebben gedaan. Zo vertellen ze dat de kunstmatige intelligentie de namen van de vogels niet heeft gebruikt. Verandert dit je antwoord op vraag 1?
3. Stel dat jij als mens geluiden zou moeten groeperen, hoe zou je dit dan doen? Denk je dat dit lijkt op hoe de kunstmatige intelligentie van dit programma het heeft gedaan?
4. Wat is het verschil tussen online en offline learning van een AI applicatie?
5. Geef in de juiste volgorde de drie stappen die gemaakt worden in supervised learning.
6. Een postcode robot krijgt jouw kerstkaart die je stuurt naar je oma onder de lens. In welke stap van supervised learning is deze robot?

:::{dropdown} Antwoorden
1. De vogels zijn gerangschikt op hun geluid. Vogels die ongeveer gelijk aan elkaar klinken zijn gegroepeerd. Dit is clustering. Er is dus unsupervised learning gebruikt. De vogels zijn ook voorzien van een naam (een etiket). Er kan dus ook supervised learning zijn gebruikt.
2. Supervised learning valt daardoor af.
3. Waarschijnlijk zouden mensen op basis van toonhoogte, frequentie en volume groeperen. Je kunt als mens redelijk eenvoudig horen wat op elkaar lijkt. Een computer vertaalt geluid naar diagrammen en doet eigenlijk beeldherkenning op die diagrammen. Het is dus niet helemaal hetzelfde.
4. Bij online learning leert de agent van de AI applicatie bij als die in bedrijf is in de test stap. Bij offline learning wordt de AI applicatie getraind. De agent die daarna in bedrijf is leert niet meer bij.
5. trainen, valideren, testen
6. De robot bevindt zich in de testfase. Hij is op dat moment in bedrijf om werkelijk het werk te doen waar de applicatie voor is ontwikkeld.
:::

::::

