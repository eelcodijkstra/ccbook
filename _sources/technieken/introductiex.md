# Introductie

Voordat we een aantal verschillende AI-technieken bekijken, stellen we eerst de  vraag: wanneer is het handig om kunstmatige intelligentie te gebruiken en wanneer niet?

Kunstmatige intelligentie heeft volgens de meeste definities iets te maken met het uitvoeren van complexe taken waarvoor intelligentie nodig wordt geacht. Er zijn echter genoeg voorbeelden van software die ook zeer complexe taken uitvoeren door gebruik te maken van heel complexe algoritmen.  Voorbeelden hiervan zijn computer algebra systemen (CAS). Met deze systemen kun je wiskundige problemen exact laten doorrekenen. Tijdens je wiskunde toetsen zouden die goed van pas komen. Helaas verboden tijdens examens. 

[[AI doet algebra?](https://www.quantamagazine.org/symbolic-mathematics-finally-yields-to-neural-networks-20200520/) Kan het nog verwarrender? De link brengt je naar een succesvolle poging om het integreren op een bepaalde manier door AI te laten doen. Het is zeker nog geen algemeen inzetbare tool.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/98dc2e72-4008-42c8-b953-e946a3b45c06/AlgebraRobot.jfif)

[AI doet algebra?](https://www.quantamagazine.org/symbolic-mathematics-finally-yields-to-neural-networks-20200520/) Kan het nog verwarrender? De link brengt je naar een succesvolle poging om het integreren op een bepaalde manier door AI te laten doen. Het is zeker nog geen algemeen inzetbare tool.

Een ander voorbeeld van complexe software zonder AI kan een robot in een productielijn zijn. Iedere keer wordt zeer precies en in de juiste volgorde een serie handelingen verricht. Er zijn echter ook weer robots in een productielijn die wel AI gebruiken om een deeltaak te verrichten. Een postsorteerrobot moet bijvoorbeeld  (handgeschreven) postcodes kunnen lezen. Lezen ofwel beeldherkenning  is een taak die we indelen bij AI. Het wordt trouwens steeds meer regel dan uitzondering dat productierobots ook van beeldherkenning gebruik maken.

## Data gestuurd

Wat maakt de intelligentie van AI nu anders dan de intelligentie in CAS systemen of andersoortige niet-AI systemen? Waarom maakt beeldherkenning een deel uit van AI en het exact oplossen van een complexe wiskundige vergelijking niet? Bekijk eerst de volgende indeling binnen de AI applicaties.

## Machine en deep learning

Ingewikkelde neurale netwerken vallen onder "deep learning". Deze groep is bevat in de groep "machine learning" van lerende AI, die weer onderdeel uitmaakt van AI in zijn geheel. We beschouwen eerst het anders zijn van machine learning en deep learning ten opzichte van niet AI-systemen.

Het verschil tussen de "niet AI-systemen" en machine learning zit in de programmeerbaarheid van een directe oplossing. De wiskunde kent een grote maar eindige overzichtelijke verzameling van bekende functies en strategieën om een wiskundig probleem op te lossen. Een CAS systeem bevat al die functies en strategieën. Geef je zo'n systeem een probleem dan kan de precieze, van te voren geprogrammeerde, oplossingsstrategie worden opgezocht en uitgevoerd.

Je hebt in de introductie het Quickdraw spel gespeeld, een applicatie gebaseerd op AI. Het heeft je vast ook verbaasd dat jouw slechte tekening werd herkend. Ook in de Quickdraw applicatie moet worden gezocht naar een oplossing van een vraag. In dit geval: In welke categorie behoort die mooie tekening? Het is zeer onwaarschijnlijk dat jouw tekening precies terug kan worden gevonden in de database van tekeningen waarop Quickdraw is gebaseerd. Sterker nog, het is zowat onmogelijk dat jouw tekening beeldpunt voor beeldpunt overeenkomt met een andere tekening. 

Er is dus wel een algoritme dat direct onderzoekt tot welke categorie jouw tekening behoort. Het stuurt jouw data door een recept (algoritme) ongeveer net zo als het CAS systeem dat doet. Maarrrrrr....., het recept dat jouw vragen beantwoordt is niet van te voren in de applicatie geprogrammeerd maar tot stand gekomen met behulp van een algoritme dat door middel van **training**  die dit recept filtert uit **data**. De mogelijkheid tot aanpassen van een applicatie aan **data** noemt men het **adaptieve vermogen.** AI toepassingen hebben alle een adaptief vermogen. De data vormt de invoer van het trainingsproces. Een AI applicatie is dus **data-gestuurd**. Het trainingsalgoritme is natuurlijk wel van te voren geprogrammeerd.

De Quickdraw app heeft dus een algoritme dat tot stand is gekomen door training, dit algoritme is niet het algoritme van het leerproces maar is het resultaat van de training. De Quickdraw app wordt dan een **agent (**vertegenwoordiger**)** genoemd van het geleerde.

Bij training is het noodzakelijk dat er een **input-output relatie** is, ofwel de data moet op de een of andere manier worden gekoppeld aan de oplossing. Je zult straks zien dat bij [winkelmandjes analyse](https://www.notion.so/3-3-Associatie-analyse-c9bc318c726243a480de86b38c390904?pvs=21) (associatie analyse) en [clustering](https://www.notion.so/7cf0b1c90c364061bc52aabe1afd4fa7?pvs=21) deze koppeling vast ligt in het trainingsalgoritme. Alleen de data zorgt dan voor de variatie in het recept. Het verkregen recept of wel het algoritme van de agent wordt een **statistisch resultaat**. ****

Bij deep learning en eenvoudigere neurale netwerken (b.v. postcode herkennen),  is ook de input-output relatie niet bekend. Bij deze vorm van AI wordt verwacht dat de training plaats vindt met input en bijbehorende output. Echter het is niet bekend hoe de relatie tussen die input en die output is. Het trainingsalgoritme heeft dan de taak de input-output relatie te schatten. Het algoritme geeft geen zekerheid over de gevonden relatie. De gevonden input-output relatie, die wordt gebruikt in de agent, is nu zelf ook een **statistisch resultaat**. 
In figuur 2 is dit weergegeven. Een applicatie die geen AI is en die eventueel gebruikt maakt van data verwerkt de invoer direct tot een uitvoer. De agents in de rechter twee diagrammen berekenen ook direct de uitvoer bij een invoer, maar kunnen dit pas nadat het algoritme in de agent door training is gemaakt.

![Figuur 2: Verschil tussen lerende en niet lerende applicaties. De agent is een zelfstandige uitvoerder (vertegenwoordiger) van het geleerde die reageert op invoer. Er zijn trouwens ook agents die zelf nog bij kunnen leren, maar die situatie is hier niet in beeld gebracht.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0e76c9ec-9b49-48ae-8099-5c821dd8acb8/App_AI_ML_DL.svg)

Figuur 2: Verschil tussen lerende en niet lerende applicaties. De agent is een zelfstandige uitvoerder (vertegenwoordiger) van het geleerde die reageert op invoer. Er zijn trouwens ook agents die zelf nog bij kunnen leren, maar die situatie is hier niet in beeld gebracht.

:::{admonition} 👓 Voorbeeld: N-term

We geven een simpel voorbeeld van een onderscheid tussen een rechttoe rechtaan berekening en één die gebaseerd is op een statistisch resultaat. Neem jouw eindrapportcijfer voor informatica. Dit cijfer is een gemiddelde van behaalde cijfers. Haal jij gemiddeld lager dan een 5,5 dan wordt jij bij de leerlingen met een onvoldoende ingedeeld. De grens 5,5 is door de school vast gekozen. Het recept is een simpele wiskundige berekening: vergelijk het cijfer met 5,5.

!https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d93184b6-fad2-4bf3-9f40-8edab943666d/fokke-en-sukke-rekenen.gif

Nu bekijken we jouw resultaat voor het wiskunde op het eindexamen. Je docent kijkt dan jouw werk na en geeft het puntentotaal door aan het College voor Examens (CVE). Het CVE krijgt de cijfers binnen van alle leerlingen die een examentoets (bijvoorbeeld wiskunde) maken, maar gebruikt slechts een deel van die cijfers voor het bepalen van de **N-term** voor dit examen. De N-term is één getal, behorend bij het examen van één vak, waarmee jouw puntenaantal wordt omgezet in een cijfer voor het examen. Leerlingen en docenten zitten na afloop van de examens in spanning af te wachten wat de N-termen voor de vakken dit examenjaar weer zullen zijn. **Deze N-termen zijn op data gebaseerd en daarom een statistisch resultaat**. Je kunt het gebruik van de N-term in het bepalen van het eindcijfer nu beschouwen als een statistisch recept  (b.v. [vwo 2-de tijdvak 2021](https://www.examenblad.nl/9336121/d/ex2021/omzet/vlk4oglb5pvs_havo_vwo_tv2/vwo-tv2.htm) , [havo 1-ste tijdvak 2019](https://www.examenblad.nl/9336119/d/ex2019/omzet/vkz5je2x54u4_havo_vwo/havo-tv1.htm)).

:::

Het voorbeeld van het examencijfer voor wiskunde is nog te simpel om er AI voor in te zetten. Er hoeft maar één getal te worden bepaald op basis van data die ook slechts uit de score van de leerlingen bestaat. [Het algoritme om de N-term te bepalen](https://www.examenblad.nl/onderwerp/n-term/2021) is daarom relatief eenvoudig. Het wordt pas nuttig om AI in te zetten als het recept of de data complex is. Deze complexiteit is er vaak al snel. Hoe kan een auto zelf rijden? Hoe herkent een postsorteerrobot een bijvoorbeeld een postcode? Hoe krijg je al die aanvullingen bij je zoekopdrachten in Google? Hoe kan ik een verzameling cd's zo goed mogelijk in groepen indelen? Hoe kan Quickdraw herkennen wat je getekend hebt? Op dit laatste voorbeeld gaan we verder in.

Het Quickdraw voorbeeld is vergelijkbaar met het postcode lezen door de robot. Voordat Quickdraw jouw plaatje kan classificeren moet er dus een classificeringsrecept worden gemaakt. Dit classificeringsrecept moet worden gemaakt op basis van voorbeeldtekeningen. Eén tekening is wel maar één datapunt, maar dit datapunt is complex. Het bestaat uit heel veel beeldpunten, namelijk de grootte van het canvas. Al die beeldpunten moeten worden meegenomen, waardoor het datapunt dus niet maar één getal is, zoals bij het N-term voorbeeld hierboven.

Om het nog lastiger te maken zijn de beeldpunten niet onafhankelijk van elkaar, een lijnstuk is een verzameling van punten. Deze relatie moet door de AI applicatie worden ontdekt. Ieder van die beeldpunten krijgt invloed door daar een getal (parameter) aan te koppelen. Net als bij de bepaling van de N-term moeten al deze parameters worden geschat. Dit gaat helaas niet in één keer. Er wordt een set parameters gekozen, dan wordt er gekeken of de output behorende bij de trainingsdata door het nieuwe recept goed worden voorspeld. Zo nee dan worden de parameters in het recept weer aangepast enz. **Het trainen van AI is in het algemeen een algoritme waarin herhaling (recursie) aanwezig is.**

## Niet lerende AI

In de bovenstaande sectie hebben we het verschil tussen een applicatie die geen AI bevat en lerende AI bekeken. Er is ook [AI die niet leert](https://www.linkedin.com/pulse/what-artificial-intelligence-without-machine-learning-claudia-pohlink). Voorbeelden voor het gebruik van AI zonder ML zijn op regels gebaseerde systemen zoals de eerste chatbots (b.v. [Eliza](https://www.chatbots.org/chatbot/eliza/), [Parry](https://www.chatbots.org/chatbot/parry/), [Jabberwacky](http://www.jabberwacky.com/)). Door de mens gedefinieerde regels laten de chatbot vragen beantwoorden en - in beperkte mate - klanten helpen . Er is geen machine learning nodig en de chatbot krijgt zijn intelligentie alleen door een grote hoeveelheid kennis door menselijke inbreng. In 1985 kreeg dit type AI zelfs een naam: [“Good Old-Fashioned Artificial Intelligence”](https://www.cambridge.org/core/books/cambridge-handbook-of-artificial-intelligence/gofai/FCF7D6DD921658FE8AE9F2A2B0FECBDD) (GOFAI). Een ander voorbeeld is natuurlijke taalverwerking (NLP), waarbij de kennis van experts met betrekking tot grammatica en de betekenis van woorden van menselijke taal wordt gecodeerd in computermodellen en methoden om taal te interpreteren en te produceren. De GOFAI bevat dus een grote hoeveelheid kennis, die moeilijk te volgen is door een enkele persoon en vaak de kennis van een enkele persoon overtreft. Deze kennis vormt de data van de applicatie en juist door de ingewikkeldheid van die data heeft men dit soort applicaties AI genoemd. 

## Kenmerken voor AI-toepassingen

Na de koppeling tussen AI en data te hebben gelegd geven we hier een aantal argumenten om AI in te zetten.

**Je kunt geen direct algoritme schrijven voor het vraagstuk.**

Bij het examencijfer voorbeeld kan de statistische N-Term met een relatief eenvoudig direct algoritme worden bepaald. Als de data complex is dan lukt dat vaak niet en wordt het vinden van het beste statistische algoritme complex.  

**De invoer die het programma krijgt, is niet volledig te bepalen en is complex .**

De invoer is bepalend voor de uitkomst van het algoritme. Als niet alle mogelijke invoer beschikbaar is (b.v. alle mogelijke schetsen van een kat) en bovendien de input niet zo simpel is dat er een direct algoritme kan worden gemaakt dan kan AI worden ingezet.  

**De oplossingsstrategie is niet bekend.**

Met behulp van kunstmatige intelligentie is het vaak mogelijk een oplossingsstrategie te vinden. Deze oplossingsstrategie is dan niet verklarend, maar werkt wel.

In de volgende secties behandelen we Machine Learning (ML). We beginnen met een algemeen deel  [machine learning](https://www.notion.so/16663254d32f42cb8e2507b3614b2e67?pvs=21)  waarin we het leerproces algemeen beschouwen. Daarna ga je leren wat de algoritmen van de meest verklaarbare ML technieken [associatie analyse](https://www.notion.so/c9bc318c726243a480de86b38c390904?pvs=21) en [cluster analyse](https://www.notion.so/7cf0b1c90c364061bc52aabe1afd4fa7?pvs=21) . Vervolgens behandelen we de minder verklaarbare resultaten van [neurale netwerken](https://www.notion.so/4778ac2fbe494b9cbe50001b3d19d1c9?pvs=21) gebruikt in deep learning (DL) en als laatste de inzet van deze technieken in [multi-agent systemen](https://www.notion.so/16663254d32f42cb8e2507b3614b2e67?pvs=21).

:::{admonition} 🛠️ Vragen

1. Leg uit wat het verschil is tussen het algoritme dat het probleem beantwoordt bij een applicatie die op AI is gebaseerd en een applicatie die dat niet is.
2. Wanneer is voor een probleemstelling kunstmatige intelligentie te gebruiken? Welke kenmerken ken je?
3. Geef een voorbeeld van een vraagstuk waar kunstmatige intelligentie toe te passen is. Geef ook aan waarom dit zo is.
4. Geef van de volgende toepassingen aan welke van de 3 kenmerken de grootste rol speelt en verklaar waarom.
    1. Suggesties voor andere producten in een webwinkel
    2. Het herkennen van postcodes
    3. Het indelen in groepjes van vergelijkbare films.
    4. ....
5. Geef de termen waarvan AI, DL, ML de afkortingen zijn en zet die in de volgende zin: ... is een onderdeel van ... dat weer onderdeel is van ...
6. Noem een techniek die onder kunstmatige intelligentie valt maar  niet onder machine learning.
7. Leg uit wat adaptief vermogen van een applicatie is.
8. Verdedig de uitspraak "Het aanscherpen van de Corona maatregelen is gebaseerd op een statistisch resultaat".
9. Verdedig de uitspraak "Het aanscherpen van de Corona maatregelen is gebaseerd op een vaste regel".
:::