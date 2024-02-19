# Associatie-analyse

Bron

In [3.1. Introductie](https://www.notion.so/3-1-Introductie-b49a35ee8d8b45bba29636e026abc2fa?pvs=21) heb je gezien dat AI applicaties data-gestuurd zijn. Hoe werkt dat sturen door data? In dit hoofdstuk en volgende hoofdstukken gaan we dat in een aantal technieken bekijken. De meeste toepassingen gebruiken artificiële intelligentie om bijvoorbeeld patronen te herkennen of groeperingen te maken. 

De berekeningen in deze paragraaf en in [cluster-analyse](cluster-analyse.md)  zijn niet heel erg ingewikkeld en zouden voor iedere leerling op havo en vwo uit te voeren moeten zijn. Lukt het niet stel dan vragen aan je docent.

Na deze paragraaf:

- Kun je in eigen woorden het doel en de taak van associatie analyse bij datamining toelichten.
- Kun je de begrippen verzamelingenleer, associatieanalyse en associatieregel uitleggen.
- Weet je de toepassingen van associatie analyse, bijvoorbeeld winkelmandjesanalyse (basket analysis).
- Ben je in staat praktische voorbeelden van associaties op te noemen.
- Kun je de berekeningen binnen het *apriori algoritme* uitvoeren, onder andere:
    - het bepalen van de doorsnede en de vereniging van twee of meer verzamelingen;
    - het berekenen van de support van een deelverzameling;
    - het vinden van de associatieregels in een eenvoudig probleem;
    - het berekenen van de betrouwbaarheid (confidence) van een associatieregel van een deelverzameling;
    - het uitvoeren van alle nodige iteraties in het apriori algoritme.
 
# Introductie

Stel je wordt manager van een supermarkt in een wijk waar veel studenten wonen. Na een paar dagen krijg je de indruk dat er veel bananen en chocolade verkocht worden. Daarom overweeg je de bananen en de chocolade samen vlak bij de kassa's te leggen om zo de klanten die langs lopen tot meer impulsaankopen te verleiden.  Je wilt als verkoper ook niet impulsief te werk gaan, dus ga je een onderzoek doen met alle kassaregistraties van de klanten als gegevens voor je onderzoek. Eén kassaregistratie geeft dan natuurlijk aan wat de klant in het winkelmandje had.  

![RumChocoBanaan1.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/861931a1-beda-4738-a550-8fac4902cdd0/RumChocoBanaan1.png)

De methoden die je als onderzoeker tot je beschikking hebt om deze gegevens te onderzoeken vallen onder *associatie-analyse*. Voor we algemeen aan de slag gaan en één van de methoden, het *apriori algoritime*, in detail uitwerken gaan we eerst intuïtief met bovenstaand voorbeeld aan de slag. Na een week heb je deze gegevens verzameld:

- er blijken 8051 klanten te zijn geweest;
- 905 keer stond banaan op de rekening;
- 750 keer stond chocolade op de rekening;
- samen kwamen bananen en chocolade 653 keer voor.

Begrippen die centraal staan in de associatie analyse zijn *support*, *associatieregel* en *betrouwbaarheid*. 

Support van één of meerdere artikelen is niets anders dan de experimentele kans dat een mandje deze artikelen bevat. Zo is $\mathrm{support}(\{\mathrm{banaan}\}) = 905/8051 \approx 0.112$ of wel ongeveer 11%. Verder is  $\mathrm{support}(\{\mathrm{chocolade}\}) = 750/8051 \approx 0.093$ en  $\mathrm{support}(\{\mathrm{chocolade}, \mathrm{banaan}\}) = 653/8051 \approx 0.081$. 

Om nu te weten te komen of het vermoeden dat bananen vaker samen met chocolade worden verkocht werkelijkheid is, ben je geïnteresseerd in de vraag: als een klant bananen koopt, hoe groot is dan de kans dat deze klant ook chocolade koopt? Ofwel hoe waar is de uitspraak: **Als een klant bananen koopt, koopt de klant ook chocolade**? Een dergelijke uitspraak noemt men een **associatieregel.**  Met de gegevens hierboven kunnen we de betrouwbaarheid (**=confidence**) van deze uitspraak uitrekenen in de vorm van een kans:

Confidence ( **Als een klant bananen koopt, koopt de klant ook chocolade ) =** 
aantal winkelmandjes met bananen en chocolade / aantal winkelmandjes met alleen bananen= 653/905=0,72.

In ongeveer driekwart van de gevallen zal de klant die bananen in zijn mandje legt doorlopen naar de chocolade. Zullen we het die klant maar eens gemakkelijker maken door deze producten dichter bij elkaar te plaatsen?

In het voorbeeld hierboven hebben we specifiek gekeken naar bananen en chocolade. Het is zinvoller als we uitgaan van alle aankopen en met een methode uitvissen wat de interessante combinaties zijn. De **apriori methode**, die we hier straks uitwerken, is zo'n methode. Eerst even een meer algemene introductie over associatie analyse.

Bij [associatie analyse](https://en.wikipedia.org/wiki/Association_rule_learning) is het de bedoeling dat een gegeven set kenmerken die een gebruiker in een toepassing aanlevert, bijvoorbeeld jouw leeftijd, geslacht, ingetypte zoekopdracht, beluisterde muziek, artikelen in je winkelmand, wordt vergeleken met dezelfde kenmerken van andere gebruikers. Gezocht wordt dan naar overeenkomsten tussen de gebruikers. Het resultaat van de associatie is dan bijvoorbeeld de uitvoer van de toepassing, bijvoorbeeld de reclame die in de zoekmachine verschijnt, muziek die jij ook wel leuk zou vinden, artikelen die jij ook zou willen kopen. Om zinvolle suggestie te doen moet een grote hoeveelheid gegevens worden geanalyseerd.

Bedrijven verkrijgen deze gegevens via de verkoopregistraties van de kassa's of via de registratie van het gebruik door personen van hun apps, bijvoorbeeld een webwinkel, sociaal medium, enzovoort. Gezocht wordt dan naar overeenkomsten tussen de personen die samengaan, zoals de gezamenlijke aankoop van bananen en chocola.

De AI techniek associatie analyse die voor deze situaties wordt gebruikt heeft als belangrijkste AI-kenmerk: *de invoer die het programma krijgt, is niet volledig te bepalen en is complex* . Het leerproces dat in associatie analyse wordt gebruikt is  *unsupervised learning*. 

Voor we de theorie van associatie analyse behandelen en leren toepassen geven we een aantal voorbeelden van gebieden waarin associatie analyse wordt gebruikt:

**Gezondheidszorg**

Artsen kunnen associatieregels gebruiken om een diagnose van patiënten te stellen. Omdat veel ziekten overeenkomstige symptomen hebben, zijn er veel variabelen waarmee rekening moet worden gehouden bij het stellen van een diagnose. Een AI applicatie met associatie analyse, die getraind is met alle symptomen en de daarbij behorende ziekten, kan een arts die ziekten tonen die het meest waarschijnlijk zijn. De arts moet daarvoor de symptomen die hij of zij ziet invoeren.

Als er nieuwe symptomen bij een ziekte optreden of als er nieuwe ziekten bijkomen, kan het machine learning-model opnieuw getraind worden met de oude en bijgewerkte gegevens.

**Detailhandel**

Detailhandelaren kunnen gegevens over aankooppatronen verzamelen en aankoopgegevens registreren en die verwerken met associatie analyse. Daarna kan dan worden gekeken welke producten het meest waarschijnlijk samen worden gekocht. De winkelier kan vervolgens de marketing- en verkoopstrategie aanpassen om van deze informatie te profiteren.

**User experience (UX) design**

Ontwikkelaars kunnen gegevens verzamelen over hoe consumenten een door hen gemaakte website/app gebruiken. Ze kunnen vervolgens associaties in de gegevens gebruiken om de gebruikersinterface van de website te optimaliseren - door bijvoorbeeld te analyseren waar gebruikers op klikken en hoe ze de kans dat een bezoeker een gewenste handeling verricht kan vergroten.

**Sociale media en entertainment**

Services zoals Facebook, Youtube, Netflix, Twitter, Spotify kunnen associatieregels gebruiken om hun engine voor contentaanbeveling van brandstof te voorzien. Machine learning-modellen analyseren gegevens over gebruikersgedrag uit het verleden op frequente patronen, ontwikkelen associatieregels en gebruiken die regels om gebruikers aanbevelingen te doen die hun ook zal interesseren, b.v. die leuke foto van een ooievaar, omdat je als vogelaar heel vaak foto's van vogels bekijkt.

# Theorie

In de opwarmer aan het begin van dit hoofdstuk hebben we geprobeerd om op een intuïtieve manier het doel van associatie analyse, een AI algoritme, duidelijk te maken. We meldden daar ook al dat we op basis van alle kassaregistraties zinvolle verbanden willen vinden. Zoals typisch is voor AI bepalen de gegevens, door deze te in te voeren in een iteratief proces, de uitkomst van de analyse.

De wiskundige techniek die wordt gebruikt in associatie analyse is gebaseerd op verzamelingen, de zogenaamde verzamelingenleer.  Het is dus nuttig eerst wat begrippen in de verzamelingenleer te introduceren. Een aantal van deze begrippen ben je waarschijnlijk al eens in de wiskundeles tegengekomen.  Daarna gebruiken we deze begrippen in de apriori methode, een veel gebruikte methode in de associatie analyse.

## Verzamelingenleer

Als leerling zit je in een klas, als voetballer zit je in een team, je play-list bevat een aantal leuke liedjes, .... Zo kunnen we nog een tijd doorgaan met het geven van voorbeelden. Voorbeelden die allemaal gaan over verzamelingen. In plaats van een klas, team, play list spreken we van een *verzameling*, in het Engels *set*. In een verzameling bevinden zich *elementen* (leerlingen, spelers, liedjes). We noteren een verzameling als volgt:

$$
\small V=\{v_1,v_2,v_3,\cdots,v_n\}
$$

Verzameling $*\small V*$ bevat elementen $*\small v*$ die we kunnen nummeren. $v_{1}$ is dan het eerste element in de verzameling, $v_{2}$ het tweede, $v_{3}$ is dan het derde, enz. De complete verzameling noteer je door accolades {..} om de lijst van elementen te zetten.

Een verzameling bestaat dus uit elementen, en als $v$ *een element is van een verzameling* $\small V$ noteren we dit wiskundig als $\small v \in V$. 

Voorbeeld: De verzameling winkelmandje met de elementen melk, brood, en kaas noteren we als:

$$
\small \text{winkelmandje} = \{\text{melk}, \text{brood}, \text{kaas}\}
$$

Als we schrijven $\small \textbf{melk} \in \textbf{winkelmandje}$, dan zeggen we dus dat melk in het winkelmandje aanwezig is.

<aside>
🚨 **Deelverzameling**

Als voor twee verzamelingen $\small X$ en $\small Y$ geldt dat elk element van $\small X$ ook een element is van $\small Y$, dan zeggen we dat $\small X$ een *deelverzameling* (of *subset*) is van $\small Y$. Notatie: $\small X⊂Y$.

</aside>

Zo geldt bijvoorbeeld voor $\small X=\{\text{melk},\text{kaas}\}$ en $\small Y=\{\text{melk},\text{brood},\text{kaas}\}$ dat $\small X ⊂ Y$, $\small X$ is een deelverzameling van $\small Y$ want melk en kaas, de elementen van $X$, zijn ook aanwezig in $Y$.

<aside>
🚨 **Doorsnede**

De *doorsnede* (of *intersection*) $\small X∩Y$ van twee verzamelingen $\small X$ en $\small Y$ bestaat uit de gemeenschappelijke elementen van $\small X$ en $\small Y$. In de figuur rechts is de doorsnede het lichtgroene gebied.

</aside>

!https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7dbb6d2a-a837-4edb-82c7-5ab602858f8c/doorsnede.svg

Zo is bijvoorbeeld de doorsnede van de verzamelingen $\small X = \{\text{melk}, \text{brood}, \text{kaas}\}$ en $\small Y = \{\text{melk}, \text{brood}, \text{pindakaas}\}$ de verzameling met melk en brood, $\small \{\text{melk}, \text{brood}\}$, want die zijn in beide verzameling aanwezig. In wiskundige notatie is dit:

$\small \{\text{melk}, \text{brood}, \text{kaas}\} \cap \{\text{melk}, \text{brood}, \text{pindakaas}\} = \{\text{melk}, \text{brood}\}$



<aside>

    
🚨 **Vereniging**

De *vereniging* (of *union*) $\small X∪Y$ van twee verzamelingen $\small X$ en $\small Y$ bestaat uit de elementen die tot $\small X$, tot $\small Y$ of tot beide horen. In de figuur rechts bestaat de vereniging uit alle enigszins gele gebieden.

</aside>

!https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e77fa85d-7f25-4332-9883-db9a7b332f1e/vereniging.svg

Zo is bijvoorbeeld de vereniging van de verzamelingen  $\small X = \{\text{melk}, \text{brood}, \text{kaas}\}$  en de verzameling $\small Y = \{\text{melk}, \text{brood}, \text{pindakaas}\}$ verzameling met de elementen Kaas, Melk, Brood en Pindakaas, $\small \{\text{melk}, \text{brood}, \text{kaas}, \text{pindakaas}\}$ want alle elementen uit $X$ en $Y$ zijn aanwezig. Notatie:

$\small \{\text{melk}, \text{brood}, \text{kaas}\} \cup \{\text{melk}, \text{brood}, \text{pindakaas}\} = \{\text{melk}, \text{brood}, \text{kaas}, \text{pindakaas}\}$

<aside>

    
🚨 **Kardinaliteit**

Voor een eindige verzameling $\small X$ definiëren we $**\small \#X**$ als het **aantal** elementen in $\small X$. Dit wordt ook wel de ***kardinaliteit*** genoemd.

</aside>

Zo is bijvoorbeeld $\small \#\{\text{chips}, \text{zeep}, \text{appels}\}=3$.

Een element van een verzameling kan zelf ook een verzameling zijn. Zo bestaat de verzameling 

$$
\small \begin{array}{rcl}C &=& \{\{\text{chips}, \text{zeep}, \text{appels}\}\\&&, \{\text{chips}, \text{zeep}, \text{appels}\}\\&&, \{\text{zeep}, \text{bananen}\}\\&&, \{\text{chips}, \text{zeep}, \text{bananen}\}\\&&\}\end{array}
$$

uit vier elementen, ieder element is een verzameling. 

Een verzameling waarin de elementen ook weer verzamelingen zijn noemt men ook wel een *collectie*.

## Associatieregels

We hadden het al over associaties tussen dataverzamelingen, tijd om dat precies te maken. Daarbij maken we gebruik van het voorbeeld hieronder. Het is een collectie van acht winkelmandjes uit een supermarkt, natuurlijk versimpeld. De meest supermarkten hebben wel vijftig soorten chocola.

$$
\small \begin{array}{lcl}C&=&\{\{\text{ melk, brood, kaas }\}\\ & & ,\{\text{ yoghurt, rozijnen, appel }\}\\ & & ,\{\text{ pindakaas, brood, melk, komkommer }\}\\ & & ,\{\text{ brood, banaan }\}\\ & & ,\{\text{ banaan, appel, chocolade }\}\\ & & ,\{\text{ brood }\}\\ & & ,\{\text{ chocolade, brood, banaan }\}\\ & & ,\{\text{ rozijnen, chocolade, pindakaas }\}\\ & & ,\{\text{ melk, brood, banaan, kaas, chocolade}\}\\ & & ,\{\text{ melk, chocolade }\}\\ & & \}\end{array}
$$

De collectie D bestaat nu uit de inhoud van de acht winkelmandjes, van iedere klant één. Ieder mandje is een verzameling van producten:

$$
\small\begin{array}{rcl}C_1&=& \{\text{ melk, brood, kaas }\} \\C_2&=& \{\text{ yoghurt, rozijnen, appel }\} \\C_3&=& \{\text{ pindakaas, brood, melk, komkommer }\} \\C_4&=& \{\text{ brood, banaan }\} \\C_5&=& \{\text{ banaan, appel, chocolade }\} \\C_6&=& \{\text{ brood }\} \\C_7&=& \{\text{ chocolade, brood, banaan }\} \\C_8&=& \{\text{ rozijnen, chocolade, pindakaas }\} \\ C_9&=& \{\text{ melk, brood, banaan, kaas, chocolade}\} \\C_{10}&=& \{\text{ melk, chocolade }\}\end{array}
$$

Om uitspraken te kunnen doen over verbanden tussen verzamelingen en de waarde van die verzamelingen zijn de volgende definities van belang.

<aside>
🚨 **Associatieregel**

De associatieregel $*\small X⇒Y*$ betekent: als de deelverzameling $*\small X*$ voorkomt dan komt ook de deelverzameling $*\small Y*$  voor. 

</aside>

Bijvoorbeeld $*\small \{\text{melk}\} ⇒ \{\text{melk},\text{brood}\}$* betekent dat als melk in een winkelmand zit, dan zit er ook brood in. In een winkelmandjes analyse is dit natuurlijk niet altijd waar, maar in associatie analyse is het van belang om te kijken hoe groot de kans op deze associatieregel is, ofwel hoe ***betrouwbaar*** is deze regel. Om de betrouwbaarheid te bepalen hebben we nog wat gereedschap nodig.

De deelverzamelingen waar we het hier over hebben zijn niet de kassabonnen zelf, maar setjes van artikelen - $*\small \{\text{melk}\} ⇒ \{\text{melk},\text{brood}\}$* - waarvan we onderzoeken of ze samen gekocht worden. Daarvoor gebruiken we de term **itemset**.

<aside>
🚨 **Itemset**

Een *itemset* is een deelverzameling van losse elementen in een collectie. Een $*\small k$-itemset* is een deelverzameling die $*\small k*$ ****elementen bevat.

</aside>

Zo algemeen geformuleerd klinkt het behoorlijk moeilijk. Bedenk dat het in ons voorbeeld gewoon gaat om setjes van artikelen die we in winkelmandjes vinden. Dat is dus een setje artikelen uit de verzameling artikelen die voorkomen:

$\small \{ \text{ melk, brood, kaas, yoghurt, rozijnen, appel ,} \\ \text{ \,\,pindakaas, komkommer, banaan, appel, chocolade } \}$

<aside>
🚨 **Support**

De *support*  van een deelverzameling $*\small X*$ is het aantal deelverzamelingen van een collectie $*\small C*$ waar de elementen van $*\small X*$ in voorkomen gedeeld door het aantal elementen van deze collectie.

$$
 ⁍
$$

Hierin is $**\small \mathrm{freq}(X)**$ het aantal (***frequentie***) van de (deel)verzamelingen waarin de elementen van $***\small X***$ voorkomen. Support is dus vaktaal voor de experimentele kans (of relatieve frequentie) dat een mandje de (deel)verzameling $***\small X***$ bevat.

</aside>

Bekijk weer de bovenstaande collectie winkelmandjes $*\small D*$ dan vind je bijvoorbeeld:

- $\small \mathrm{freq}(\{\text{banaan}\})=4$, want er zijn 4 elementen in C waartoe element banaan behoort, namelijk $\small C_{4},C_{5},C_{7},C_{9}$.
- $*\small \mathrm{support}(\{\text{melk}\})=\frac{4}{8}*$, want er zijn $\small \mathrm{freq}(\{\text{melk}\})=4$ van de $\small \#C=10$ elementen van $\small C$ waar het element $*\small \text{melk}*$ in voorkomt.
- $\small \mathrm{support}(\{\text{banaan},\text{chocolade}\})=\frac{3}{10}$, want er zijn 3 van de 10 deelverzamelingen waarin de elementen banaan en chocolade samen voorkomen.

Nog een voorbeeld van een praktische toepassing. Bij marktonderzoek is de support van een stel artikelen (bijvoorbeeld $*\small K=\{\text{televisie},\text{surroundset}\}*$) het aantal klanten dat al die artikelen samen koopt, op het totaal aantal klanten, meestal weergegeven als percentage.

In de associatieanalyse kan niet altijd alles worden meegenomen. Vaak is men alleen geïnteresseerd in artikelen en combinaties van artikelen die vaak voorkomen en dus frequent zijn.

<aside>
🚨 **Frequent**

Een stel artikelen $***\small K*$** met hoge support, boven een zekere drempel, heet ***frequent***. Ofwel: ten opzichte van het totaal aantal klanten kopen veel klanten alle artikelen in $***\small K***$.

</aside>

In de associatieanalyse, bijvoorbeeld bij de winkelmandjes, wil men handelen op basis van associatieregels. Deze associatieregels stelt men dan op voor frequente itemsets. Maar dat is niet voldoende, de associatieregel moet ook nog interessant zijn. De kans op de associatie moet vrij groot zijn. Het heeft niet veel zin om te gaan adverteren voor Y bij mensen die X kopen, als uit de data helemaal niet blijkt dat X-kopers vaak Y kopen. We willen weten of de associatie vaak voorkomt. In de vaktaal heet dat de **confidence** ofwel de **betrouwbaarheid** van de associatieregel.

Laten we terugkeren naar het voorbeeld van de bananen en de chocolade. We hebben tien winkelmandjes. Banaan zit in vier van die winkelmandjes en drie van de vier bevatten weer chocolade. Dat is 75%, een kans van driekwart dat de associatie optreedt. Nu is een collectie van tien winkelmandjes niet echt groot genoeg om die kans echt te bepalen, maar wanneer je zo een miljoen winkelmandjes onderzoekt, is de kans behoorlijk zeker.
De betrouwbaarheid van een associatieregel bepalen we dus zo.

<aside>
🚨 **Betrouwbaarheid**

De *betrouwbaarheid* (of *confidence*) van de associatieregel $*\small X⇒Y*$ wordt berekend door de support van de vereniging van $*\small X*$ en $*\small Y*$ te delen door de support van $*\small X*$.

$$
\small \mathrm{confidence}(X \Rightarrow Y) = \frac{\mathrm{support}(X \cup Y)}{\mathrm{support}(X)}
$$

Je kunt dit ook simpeler uitrekenen door de frequenties op elkaar te delen, dit geeft dezelfde uitkomst.

$$
\small \mathrm{confidence}(X \Rightarrow Y) =\frac{\mathrm{freq}(X \cup Y)}{\mathrm{freq}(X)}
$$

</aside>

In ons voorbeeld kunnen we de betrouwbaarheid van de associatieregel
$\{\small \text{ banaan } \} \Rightarrow \{\small \text{ banaan, chocolade } \}$ dus uitrekenen door de support te delen: 3/10 gedeeld door 4/10. Of simpeler, door de frequenties op elkaar te delen: 3/4.

## Apriori algoritme

Er bestaan veel algoritmes om associatieregels te ontdekken. De oudste en meest bekende methode is het Apriori algoritme (a priori bekent: op basis van eerder onderzoek) ontwikkeld voor transacties (verkopen). Het is in de jaren negentig bedacht door [Agrawal en collega's](https://en.wikipedia.org/wiki/Apriori_algorithm).

Met het algoritme vind je interessante associatieregels voor producten die voldoende frequent gekocht worden. Voldoende voorkomend (frequent) betekent in dit geval dat we niet alle verbanden even nuttig vinden. Als producten te weinig voorkomen, ofwel te weinig support hebben, dan nemen we die niet mee in het algoritme.

Je geeft een ondergrens aan de support op, de **minimale support**.

Naast deze minimale support kun je ook instellen hoe betrouwbaar de associatieregels moeten zijn (hoe sterk zijn de aanwijzingen), ofwel je geeft een **minimale confidence** op.

<aside>
🚨 Apriori algoritme

Het Apriori algoritme voor een collectie *C* bestaat uit de volgende twee fasen:

1. Het maken van een collectie *F* met verzamelingen die voldoende frequent (groter dan een minimale support) zijn in *C*,
2. Het opstellen van associatieregels met verzamelingen uit *F* met voldoende betrouwbaarheid (groter dan een minimale confidence) in *C*.
</aside>

### **voorbeeld:**

We gaan door deze twee fasen heen aan de hand van de collectie winkelmandjes die we al eerder gebruikten. Die is klein, in echte toepassing zijn dat er duizenden, of miljoenen.

$\small \begin{array}{lcl}C&=&\{
\{\text{ melk, brood, kaas }\}\\ & & ,
\{\text{ yoghurt, rozijnen, appel }\}\\ & & ,
\{\text{ pindakaas, brood, melk, komkommer }\}\\ & & ,
\{\text{ brood, banaan }\}\\ & & ,
\{\text{ banaan, appel, chocolade }\}\\ & & ,
\{\text{ brood }\}\\ & & ,
\{\text{ chocolade, brood, banaan }\}\\ & & ,
\{\text{ rozijnen, chocolade, pindakaas }\}\\ & & ,
\{\text{ melk, brood, banaan, kaas, chocolade}\}\\ & & ,
\{\text{ melk, chocolade }\}\\ & & \}
\end{array}$

De centrale vraag is: welke combinaties van producten zijn interessant? We vinden combinaties interessant als er een minimale support is van 0.3 (of 30%) en we zijn alleen geïnteresseerd in associatieregels met een betrouwbaarheid van minimaal 70%.

### Fase1: Het maken van een collectie *F* met verzamelingen die voldoende frequent (groter dan een minimale support) zijn in *C*

Het algoritme bouwt een verzameling van frequente itemsets op. Dat gaat van onderop ("bottom up"): eerst itemsets van 1 item, dan van 2, enzovoort. Probleem is dat het aantal itemsets erg groot wordt, als de winkel veel artikelen heeft. Bij duizend artikelen heb je al meer dan 100 miljoen setjes van drie artikelen! Het algoritme gebruikt een truc om niet zoveel itemsets te hoeven bekijken. Zometeen meer daarover.

Na de start van het algoritme maken we eerst de lege collectie $F = \{\}$ en zetten het aantal elementen $k$ aanwezig in een itemset op 0. Gelijk daarna maken we $k$ gelijk aan 1 en gaan we naar het oranje blok:

<aside>
🚨 **Genereer alle kandidaat itemsets met lengte 1**

We verzamelen de 1-itemset in de collectie $*S_1*$. De collectie $*S_1*$ bestaat dan uit alle verzamelingen met slechts één item. (b.v. alle verschillende artikelen die je in al de winkelmandjes tegenkomt). 

**voorbeeld:**

$*\small S_1= \{ \text{ melk, brood, kaas, yoghurt, rozijnen, appel,} \\ \text{ pindakaas, komkommer, \, banaan, appel, chocolade } \}*$

</aside>

Vervolgens gaan we naar de stap in het blauwe blok: 

<aside>
🚨 **Bereken de support van elke 1- itemset uit $S_1$ in C**

$$
\begin{array}{ll}\colorbox{red}{\color{white} \text{Support in C}}\\ \colorbox{red}{\color{white}\text{Element in } S1}  & \colorbox{red}{\color{white}\text{Support}}\\\{melk\} & 40\% \\\{brood\}& 60\%\\\{kaas\}& \color{red}20\% \\\{yoghurt\}& \color{red}10\% \\\{rozijnen\}& \color{red}20\% \\\{appel\}& \color{red}20\% \\\{pindakaas\}& \color{red}20\% \\\{komkommer\}& \color{red}10\% \\\{banaan\}& 40\% \\\{chocolade\}& 50\% \end{array}
$$

</aside>

Als laatste gaan we in de eerste iteratie naar het paarse blok:

<aside>
🚨 **Voeg de 1-itemsets met voldoende support toe aan de collectie *F***

**voorbeeld:**

In de tabel hierboven zie je dat alleen $\{melk\}$,$\{brood\}$,$\{banaan\}$  en $\{chocolade\}$ de grens van 30% halen. De collectie $F$ met itemsets met voldoende support breiden we dus uit met deze vier 1-itemsets.

$$
F=\{Spaghetti\},\{Tomatensaus\}, \{Brood\}
$$

</aside>

We komen nu aan bij de test "Is er in deze ronde een k-itemset aan *F* toegevoegd?". In het voorbeeld hebben we net vier verzamelingen met 1-item toegevoegd en is het antwoord dus ja, we  zijn dus nog niet klaar. We verhogen k naar 2 en gaan weer verder bij het oranje blok:

<aside>
🚨 **Genereer alle kandidaat itemsets met lengte 2**

We verzamelen de 2-itemset in de collectie *S2*. De collectie *S2* bestaat dan uit alle verzamelingen met twee items waarbij we alleen nog kijken naar de items die in *F* aanwezig zijn. 

**voorbeeld:**

$$
*S*2=\{Spaghetti, Tomatensaus\}, \{Spaghetti, Brood\}, \{Tomatensaus, Brood\}
$$

</aside>

De truc van het algoritme is dat we niet alle combinaties van twee artikelen bekijken, maar alleen de - nu vier - frequente artikelen gebruiken. Het heeft geen zin een combinatie met een niet-frequent artikel te bekijken. Apart komt dat al te weinig voor, laat staan in combinatie. We gaan dus door met de vier items uit ronde 1, die samen zes combinaties leveren. 

<aside>
🚨 **voorbeeld:**

$S_{2}=\{\{melk,brood\},\{melk,banaan\},\{melk,chocolade\},\\
\{brood, banaan \}, \{brood, chocolade \}, \{banaan, chocolade \}\}$

</aside>

Op naar het blauwe blok om de support te berekenen:

<aside>
🚨 **Bereken de support van elke 2- itemset uit S2 in C**

**voorbeeld:**

$$
\begin{array}{ll}\colorbox{red}{\color{white} \text{ Support in C}}\\ \colorbox{red}{\color{white}\text{Element in S2}} & \colorbox{red}{\color{white}\text{Support}}\\\{melk,brood\} & 30\% \\\{melk,banaan\}& \color{red} 10\%\\\{melk,chocolade\}& \color{red} 20\%\\\{brood, banaan\}& 30\% \\\{brood, chocolade\}& \color{red} 10\%\\\{brood, banaan\}& 30\% \end{array}
$$

</aside>

Kunnen we weer itemsets toevoegen aan *F*?

<aside>
🚨 **Voeg de 2-itemsets met voldoende support toe aan de collectie *F***

**voorbeeld:**

In de tabel hierboven zie je dat niet alle 2-itemsets de grens van 30% halen. De collectie $F$ met itemsets met voldoende support breiden we dus alleen uit met de 2-itemsets
$\{melk,brood\}, \{brood, banaan \}$ en \{banaan, chocolade\}.

$\begin{array}{ll}  F= & \{\{melk\}, \\ 	&  \{brood\}, \\	&  \{banaan\}, \\	&  \{chocolade\}, \\	&  \{melk,brood\}, \\	&  \{brood, banaan\}, \\	&  \{banaan, chocolade\} \}\end{array}$

</aside>

We komen nu weer aan bij de test "Is er in deze ronde een k-itemset aan *F* toegevoegd?". In het voorbeeld hebben we er weer drie toegevoegd en is het antwoord dus ja, we  zijn dus nog steeds niet klaar. We verhogen k naar 3 en gaan weer verder bij het oranje blok:

<aside>
🚨 **Genereer alle kandidaat itemsets met lengte 3**

We verzamelen de 3-itemset in de collectie *S3*. De collectie *S3* bestaat dan uit alle verzamelingen met drie items waarbij we alleen nog kijken naar de items die in *F* aanwezig zijn. 

**voorbeeld:**

$S_{3}=\{\{melk, brood, banaan \}, \{melk, brood, chocolade \}, \\ \,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\{brood, banaan, chocolade \} \}$

</aside>

Het blauwe blok levert nu de support:

<aside>
🚨 **Bereken de support van elke 3- itemset uit S3 in C**

**voorbeeld:**

$$
\begin{array}{ll}\colorbox{red}{\color{white} \text{ Support in C}}\\ \colorbox{red}{\color{white}\text{Element in S3}} & \colorbox{red}{\color{white}\text{Support}}\\\{melk, brood, banaan\} & \color{red} 10\% \\\{melk, brood, chocolade\} & \color{red} 10\% \\\{brood, banaan, chocolade\} & \color{red} 10\% \\\end{array}
$$

</aside>

Kunnen we weer itemsets toevoegen aan *F*?

<aside>
🚨 **Voeg de 3-itemsets met voldoende support toe aan de collectie *F***

**voorbeeld:**

In de tabel hierboven zie je dat alle 3-itemsets de grens van 20% niet halen. Er kan niets aan F worden toegevoegd. De collectie F blijft dus:

$*\begin{array}{ll}  F= & \{\{melk\}, \\ 	&  \{brood\}, \\	&  \{banaan\}, \\	&  \{chocolade\}, \\	&  \{melk,brood\}, \\	&  \{brood, banaan\}, \\	&  \{banaan, chocolade\} \}\end{array}*$

</aside>

We komen nu weer aan bij de test "Is er in deze ronde een k-itemset aan *F* toegevoegd?". In het voorbeeld hebben we niets meer hebben toegevoegd dus nee, we  zijn klaar en eindigen met de bovenstaande verzameling $F$ verzameling

In het voorbeeld zijn in het algoritme dus 3 iteraties nodig geweest om het proces te stoppen. Andere samenstellingen van de winkelmandjes met vooral meer artikelen zal ervoor zorgen dat er veel meer iteraties nodig zijn. 

We zijn nu aan het eind van fase 1 gekomen en gaan nu kijken welke associatieregels interessant zijn.

### Fase 2: Het opstellen van associatieregels met verzamelingen uit *F* met voldoende betrouwbaarheid (groter dan een minimale confidence) in *C*.

Als de collectie $F$ is gevonden kunnen we met de verzamelingen in $F$ associatieregels gaan maken. Voor elke associatieregel bepalen we de confidence. Alleen in die associatieregels met voldoende confidence zijn we geïnteresseerd.

Nu is een associatieregel van de vorm: "Als een klant artikel(set) X koopt, koopt de klant dan ook artikel Y". In formule - voor het voorbeeld waarmee we dit onderwerp begonnen: $\{banaan\} \Rightarrow \{banaan, chocolade\}$.

In zo'n regel staan dus rechts meer items dan links. We kunnen rechts dus de drie 2-itemsets uit $F$ zetten. Bij elk kunnen we twee associatieregels onderzoeken. Naast $\{banaan\} \Rightarrow \{banaan, chocolade\}$ is dat ook $\{chocolade\} \Rightarrow \{banaan, chocolade\}$. Zo krijgen we de zes mogelijke associatieregels in de tabel hieronder. Voor elke regel delen we de support van de betrokken itemsets.

### Fase 2: Het opstellen van associatieregels met verzamelingen uit *F* met voldoende betrouwbaarheid (groter dan een minimale confidence) in *C*.

Als de collectie $F$ is gevonden kunnen we met de verzamelingen in $F$ associatieregels gaan maken. Voor elke associatieregel bepalen we de confidence. Alleen in die associatieregels met voldoende confidence zijn we geïnteresseerd.

Nu is een associatieregel van de vorm: "Als een klant artikel(set) X koopt, koopt de klant dan ook artikel Y". In formule - voor het voorbeeld waarmee we dit onderwerp begonnen: $\{banaan\} \Rightarrow \{banaan, chocolade\}$.

In zo'n regel staan dus rechts meer items dan links. We kunnen rechts dus de drie 2-itemsets uit $F$ zetten. Bij elk kunnen we twee associatieregels onderzoeken. Naast $\{banaan\} \Rightarrow \{banaan, chocolade\}$ is dat ook $\{chocolade\} \Rightarrow \{banaan, chocolade\}$. Zo krijgen we de zes mogelijke associatieregels in de tabel hieronder. Voor elke regel delen we de support van de betrokken itemsets.

n de eerste regel in de tabel hierboven geeft voor associatieregel 
{banaan}⇒{banaan,chocolade} een betrouwbaarheid van 75%. Dit zegt dat in 75% van de gevallen dat een banaan koopt, deze ook chocolade gaat kopen. 75% is groter dan 70%, voldoende betrouwbaar dus. De derde regel laat zien dat als iemand brood koopt, deze persoon in 50% van de gevallen een banaan koopt, te weinig voorspellend om rekening mee te houden want kleiner dan 70%. Dus blijven over de associatieregels

Tijd om dit zelf toe te passen:
