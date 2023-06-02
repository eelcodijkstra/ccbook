# 2.2. De FAST-principes

Het gebruik van AI in bedrijven, publieke organisaties en binnen overheden brengt altijd risico's met zich mee. Soms wordt AI ingezet op een manier die niet voor iedereen even eerlijk is, of die ondoorzichtig is. Daardoor kun je niet controleren wat er nu precies gebeurt in zo'n AI-systeem.  De term **black box** komt je misschien wel bekend voor. In AI is er sprake van een black-boxsysteem als het AI-systeem inzichten produceert op basis van data, terwijl de eindgebruiker en vaak ook de ontwikkelaar niet weten hoe die inzichten tot stand komen. Een bekend voorbeeld is onderzoek van het MIT Media Lab, waaruit bleek dat in veel AI voor gezichtsherkenning de gezichten van mannen veel beter worden herkend dan die van vrouwen. Ook scoorde de gezichtsherkenning slechter bij een donkere huid. Bekijk het filmpje 'Gender Shades' maar eens. (De video is Engelstalig. Je kunt ondertiteling aanzetten en automatische vertaling instellen door in de video rechts onderaan op ⚙️/Instellingen te klikken, bij Ondertiteling te kiezen voor Automatisch vertalen en de juiste taal te selecteren.)

[https://youtu.be/TWWsW1w-BVo](https://youtu.be/TWWsW1w-BVo)

<aside>
🛠️ **Vragen**

1. Kun je zelf nog wat andere voorbeelden noemen van een AI-systeem dat ondoorzichtig of niet eerlijk is? Zoek op internet naar leuke en aansprekende voorbeelden en probeer minimaal drie verschillende 'foute' AI-toepassingen te noemen. Geef daarbij aan waarom ze 'fout' waren. Hoe zou zo'n systeem volgens jou verbeterd kunnen worden?
</aside>

- Antwoorden
    1. Wat mogelijke voorbeelden van niet eerlijke of ondoorzichtige AI-toepassingen: 
        - In [april 2021](https://nos.nl/artikel/2378060-veel-onduidelijk-over-deepfake-gesprek-van-kamerleden-met-medewerker-navalny) voerden Nederlandse Kamerleden een gesprek met iemand die zich schijnbaar voordeed als Leonid Volkov, een hooggeplaatste medewerker van de Russische oppositieleider Navalny. Navalny zit in een Russisch strafkamp en was op dat moment in hongerstaking uit protest tegen zijn behandeling en gebrek aan medische hulp. Er werd aanvankelijk gedacht dat er van AI gebruik was gemaakt om zo een 'deepfake'-gesprek te voeren, maar uiteindelijk bleek dat het niet om AI ging, maar om twee Russische 'grappenmakers'. Kunstmatige intelligentie, de macht van techbedrijven, de datahonger van de overheid, de Tweede Kamer heeft er weinig grip op, zo oordeelde zij daarna zelf. Daarom komt er nu een [speciale commissie](https://nos.nl/nieuwsuur/video/2382323-een-speciale-commissie-is-volgens-adviseurs-hoog-nodig) die de macht beter moet controleren. En dat is hoognodig, zo vinden verschillende adviseurs.
        - In [februari 2020](https://nos.nl/artikel/2369502-weer-iemand-ontslagen-bij-ethisch-onderzoeksteam-google) heeft Google het hoofd van een ethisch onderzoeksteam bij het bedrijf ontslagen. Onderzoeker Margaret Mitchell maakte dat zelf bekend op Twitter. Mitchell deed samen met andere wetenschappers onderzoek naar ethische kwesties rond kunstmatige intelligentie. Volgens haar en mede-onderzoeker Timnit Gebru waren diversiteit en inclusie bij Google ver onder de maat. Ze waren ook bang dat het bedrijf hun onderzoek zou censureren. Google beloofde de onderzoekers dat ze vrijelijk te werk konden gaan. Maar die belofte leek onder druk te staan toen de onderzoekers ook wilden publiceren over de negatieve effecten van Googles technologie en producten. Een vorm van ondoorzichtige AI dus...
        - In [december 2020](https://nos.nl/artikel/2362487-honderden-klachten-na-deepfake-kersttoespraak-met-dansende-koningin-elizabeth) klaagden meer dan tweehonderd mensen bij de Britse mediawaakhond Ofcom over een satirische kersttoespraak van koningin Elizabeth, die tegelijk werd uitgezonden met de echte kerstboodschap van de Queen. In de 'deepfake'-video liet omroep Channel 4 de 94-jarige koningin onder meer voor de kerstboom op haar bureau dansen.
        - In 2017 implementeerde Amazon een [AI-tool](https://www.businessinsider.nl/amazon-built-ai-to-hire-people-discriminated-against-women-2018-10?international=true&r=US) om er personeel mee te werven, maar het bedrijf stopte met het project nadat was gebleken dat de tool vrouwen discrimineerde. Software engineers vonden naar verluidt dat de AI ongunstig was voor vrouwelijke kandidaten, omdat door mannen gedomineerde cv's waren gebruikt om gegevens te verzamelen.

AI-systemen zijn gebouwd op data. Een groot deel van deze data komt uit het verleden, toen we wel data konden verzamelen, maar die nog niet konden verwerken. Dit betekent dat veel historische vooroordelen in onze samenleving naar boven borrelen wanneer we een systeem gebaseerd op historische data gebruiken om de toekomst te voorspellen en vorm te geven. In dit geval bieden in het verleden behaalde resultaten wél een garantie voor de toekomst! Dit soort vooroordelen in zelf-beslissende netwerken heeft negatieve gevolgen voor de echte wereld, voor mensen die naast een baan grijpen of slechte cijfers halen die ze niet verdienen. En geen enkele manager wil dat het AI-systeem van zijn organisatie in negatieve zin de kranten haalt. Het is dus de moeite waard om vooruit te denken om mogelijke problemen te vermijden.

<aside>
🛠️ **Opdracht**

Bekijk de onderstaande videoles 'Afleiding in het verkeer', waarin Marius Kok van de Nationale Politie de Monocam bespreekt: een AI-toepassing die controleert of automobilisten tijdens het rijden een mobiele telefoon in hun hand hebben. In het vervolg van deze les komen we terug op de in de video gepresenteerde Monocam.

(De video is Engelstalig, maar je kunt Nederlandse ondertiteling aanzetten.)

[https://youtu.be/SB23SooOMmc](https://youtu.be/SB23SooOMmc)

</aside>

## Ethische aspecten

Ethische bedreigingen die bij AI-applicaties een grote rol spelen, zijn onder meer **vooringenomenheid** (of **bias**), het probleem van **ondoorzichtigheid** **(of **opacity**) en de mogelijkheid van **discriminatie**.

**Vooringenomenheid** wil zeggen dat iemand al een oordeel klaar heeft voordat hij de feiten onder ogen krijgt. De Toeslagenaffaire bijvoorbeeld, toont (onder meer) aan hoe belangrijk het is om vooringenomenheid te voorkomen. Het staat inmiddels vast dat de Belastingdienst een “institutioneel vooringenomen” werkwijze heeft gehanteerd: grote groepen burgers zijn op grond van afkomst gekwalificeerd en als fraudeur weggezet.

**Ondoorzichtigheid** gaat erover dat iets niet goed te begrijpen is. Als voor een AI-systeem niet kan worden uitgelegd hoe dit systeem tot besluiten komt, is deze besluitvorming ondoorzichtig, oftewel een black-boxsysteem. Ondoorzichtigheid is natuurlijk niet alleen een AI-probleem. Wanneer iemand bijvoorbeeld erg onduidelijk is over de besteding van zakgeld, kun je zeggen dat “zijn uitgavenpatroon erg ondoorzichtig is”.

**Discriminatie** is letterlijk: het maken van onderscheid. Het gaat dan in AI-applicaties over het ten onrechte maken van onderscheid  tussen mensen of groepen, oftewel het niet gelijk behandelen van gelijke gevallen. Bij sollicitaties blijft dit bijvoorbeeld een [belangrijk probleem](https://www.werf-en.nl/algoritmes-tijdens-de-sollicitatieprocedure-discrimineren-ze-nou-of-niet/).

Dergelijke bedreigingen zijn met elkaar verbonden. Vooringenomenheid kan schuilen in complexe, ondoorzichtige modellen, met discriminatie tot gevolg. In plaats daarvan willen we dat onze AI-systemen eerlijk en verklaarbaar zijn en op een goede manier met gegevens omgaan.

![Het doolhof van de zoektocht naar verantwoorde AI [Bron](https://sherpa.ai/blog/the-ethics-of-ai-in-europe/)](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6cc6f19f-b701-4379-8e87-03960eeb4f9f/ethics.jpg)

Het doolhof van de zoektocht naar verantwoorde AI [Bron](https://sherpa.ai/blog/the-ethics-of-ai-in-europe/)

### Vooringenomenheid (bias)

Vooringenomenheid of bias kan in het geval van een AI-toepassing ontstaan door bijvoorbeeld data waarin die vooringenomenheid al aanwezig is, zoals in het voorbeeld van Gender Shades. Maar het kan ook zijn dat de gebruikte algoritmen niet neutraal zijn. Soms zijn meningen direct in code ingebed.

Denk bijvoorbeeld maar eens aan koken. Een recept is eigenlijk een soort algoritme. Het doel is om een maaltijd samen te stellen. De ingrediënten en hoeveelheden van elk ingrediënt die je nodig hebt, zijn daarbij de parameters van een model. Een belangrijk aspect bij het schrijven van zo'n recept is het definiëren van succes: wanneer is een maaltijd geslaagd? Misschien geef je veel om een stevige smaak en moet je recept daarom juist veel vet, zout en suiker bevatten. Maar anderen vinden wellicht hun gezondheid belangrijk en stoppen vooral veel voedingsstoffen in hun recept, terwijl het weinig vet, zout en suiker bevat. Zo'n definitie van succes bevat daarom ook altijd meningen én vooroordelen.

Hetzelfde geldt voor een algoritme. Een model dat optimaliseert voor een bepaalde definitie van succes is niet per se neutraal. Het is belangrijk om hier rekening mee te houden: een rekruteringsalgoritme, een algoritme dat helpt bij het aannemen van nieuw personeel, kan worden geoptimaliseerd om werknemers te selecteren die het meeste geld voor een bedrijf verdienen, maar dit gaat ten koste van teamwerk of moreel gedrag. Een organisatie moet goed nadenken over deze afwegingen, en besluiten wat zij wil optimaliseren. Onthoud daarom dat AI geen volledig neutrale beslissing kan garanderen, maar besef ook dat een mens dat net zomin kan.

<aside>
🛠️ **Vragen**

1. Waarom kunnen gegevens uit het verleden leiden tot vooringenomenheid bij de besluitvorming door AI?
2. Wat hebben de makers van de Monocam, zoals gepresenteerd in de bovenstaande videoles 'Afleiding in het verkeer' van de Nationale Politie, gedaan om vooringenomenheid of bias te voorkomen?
3. Zoek op internet nog een tweetal voorbeelden van vooringenomenheid. Dit hoeft niet direct in een AI-applicatie te zijn.
</aside>

- Antwoorden
    1. Gegevens uit het verleden komen uit een situatie die nu mogelijk niet meer van toepassing is. Op dit moment zijn mensen bijvoorbeeld gemiddeld zwaarder dan vroeger. Train je dan een applicatie waarin het gewicht van een persoon een factor is, dan kan het niet anders dan dat de applicatie fouten maakt als de trainingsdataset gemiddeld lichtere personen bevat.
    2. Er is goed nagegaan of in een beeld echt een mobiel te zien is. De data wordt voorzien van een oordeel van een professional en de uitvoer laat alleen de mobiel en het nummerbord zien. De uitvoer wordt achteraf ook nog beoordeeld door de agenten. Gezichten worden vervaagd om te voorkomen dat een agent daardoor een discriminerend oordeel velt.
    3. Zelf doen en met klasgenoten bediscussiëren.

### Doorzichtigheid

Een tweede en aanverwant probleem is ondoorzichtigheid. We staan hier nog even stil bij het begrip **black box**. Meestal verwijst dit begrip naar complexe modellen, zoals neurale netwerken of deep learning algoritmen, die zichzelf versterken en moeilijk te controleren zijn omdat ze zoveel berekeningen bevatten. Maar ondoorzichtigheid, het probleem van niet begrijpen wat AI van plan is, kan ook van toepassing zijn op veel eenvoudigere algoritmen. Laten we eens kijken waarom.

Er kunnen verschillende bronnen van ondoorzichtigheid zijn als het gaat om AI; het gaat niet alleen om complexiteit:

1. Bewust vaag houden vanwege concurrentievoordeel:  bedrijven willen soms niet dat iemand hun algoritme begrijpt, want een algoritme kan een belangrijke bron van concurrentievoordeel zijn. De werking van een algoritme geheimhouden kan ook *gamen* van een algoritme voorkomen. Als sollicitanten bijvoorbeeld weten naar welke trefwoorden een algoritme in een cv zoekt, kunnen ze deze woorden gewoon in het document plaatsen om geselecteerd te worden. 
2. Een vrij lage technische geletterdheid onder de algemene bevolking: zelfs een eenvoudig algoritme kan voor veel mensen moeilijk te begrijpen zijn. 
3. Mensen en machines redeneren anders: het is bijvoorbeeld moeilijk voor een AI-systeem om uit te leggen waarom het denkt dat het naar een kat kijkt, terwijl een mens dat moeiteloos kan uitleggen. 
4. Leveranciershype: bedrijven verkopen soms nep-AI. Ze beweren bijvoorbeeld dat ze een nieuwe geavanceerde chatbot hebben, maar deze wordt feitelijk aangedreven door mensen. Soms wordt een media-rage strategisch gebruikt om te verbergen wat er echt achter de schermen gebeurt.

<aside>
🛠️ **Vragen**

1. Waarom worden sommige AI-toepassingen 'black-boxalgoritmen' genoemd? Wat zou daarvoor een oplossing kunnen zijn?
2. Waarom zou een bedrijf nep-AI willen verkopen? Kun je een voorbeeld noemen?
</aside>

- Antwoorden
    1. De grootte van de dataset en het leerproces op deze dataset zorgen voor een ondoorzichtig eindproduct. Het is niet mogelijk deze ondoorzichtigheid helemaal op te heffen. Er moet vooral goed over de dataset worden nagedacht. Een andere oplossing zou zijn om een AI-vrije applicatie te maken, maar dan moeten de regels om van invoer naar  uitvoer te komen wel bekend zijn. AI is er echter juist om deze onbekende regels te ontdekken.
    2. AI is in de mode, dus een bedrijf kan proberen daar gebruik van te maken om meer geld te verdienen.

### Discriminatie

De meeste organisaties willen niemand discrimineren. Maar ze hebben soms niet door dat hun systemen discriminerende gevolgen hebben, zeggen onderzoekers die het effect van discriminatie op AI bestuderen. AI kan bijvoorbeeld mensenrechten en andere belangrijke waarden bedreigen, zoals het recht op non-discriminatie. Een van de problemen is dat AI onbedoeld kan leiden tot ongeoorloofde en oneerlijke discriminatie. Dat kan onder meer gebeuren als een AI-systeem leert van menselijke beslissingen die discrimineren. 

Om mensen tegen oneerlijke discriminatie door AI te beschermen, is aanvullende regelgeving nodig. Zo simpel is dat echter ook weer niet, want het gebruik van AI-systemen is te gevarieerd voor één set regels. In verschillende sectoren staan verschillende waarden op het spel. Daarom worden vaak sectorspecifieke regels overwogen. Verderop in deze les leer je meer over de regelgeving rondom AI.

<aside>
🛠️ **Vragen**

1. Heeft uitsluitend kwaadaardig gebruik van AI negatieve gevolgen voor de maatschappij? Of kan ook goedbedoeld gebruik van AI leiden tot negatieve gevolgen?
2. Waarom hangen vooringenomenheid, ondoorzichtigheid en discriminatie samen?
</aside>

- Antwoorden
    1. Dat ook goedbedoelde AI problemen kan geven, kunnen we illustreren met een voorbeeld uit de criminaliteitsbestrijding. Als alle gegevens van misdadigers worden gebruikt om potentiële misdadigers op te sporen, is er sprake van een goed doel om misdaad te voorkomen. Toch zullen er volledig onschuldige personen worden aangewezen als mogelijke misdadigers.
    2. Als we bewuste ondoorzichtigheid en discriminatie buiten beeld laten, kan een onbedoelde vooringenomenheid van de dataset er door het ondoorzichtige leerproces voor zorgen dat er onbedoeld discriminatie optreedt.

## De FAST-principes

Dus hoe open je die zwarte doos van AI, om ervoor te zorgen dat je alleen eerlijke, verklaarbare, veilige en transparante AI-systemen gebruikt? Het is natuurlijk allereerst belangrijk dat je op de hoogte bent en blijft van de ontwikkelingen. Volg opleidingen om te snappen wat de techneuten bedoelen, en volg je instinct. Maar daarnaast investeren allerlei organisaties in protocollen en standaarden voor een eerlijk, verantwoord en transparant gebruik van AI. Daarin staan vaak de zogeheten FAST-principes centraal: FAST staat daarbij voor *fairness*, *accountability*, *safety* en *transparency*. 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/26a4b338-b2f2-45d7-8327-62983ff88e2c/FAST.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/26a4b338-b2f2-45d7-8327-62983ff88e2c/FAST.png)

### Fairness

Het is belangrijk om je te realiseren dat AI-systemen zijn ontworpen door mensen die gebonden zijn aan de beperkingen van hun context en vooroordelen. Zo zal ieder AI-systeem racistisch zijn ten gunste van zijn makers; een Japanse AI-toepassing zal totaal anders redeneren dan een Amerikaanse of Duitse, omdat de sociale waarden in deze landen verschillen. Als je als gebruiker weet dat een AI-systeem met vooringenomenheid gebouwd is, kun je er ook op anticiperen. 

De beperkingen in de context kunnen dus in de systemen terechtkomen. Er kan bijvoorbeeld bias (vooringenomenheid ) optreden bij het verzamelen en analyseren van gegevens. Het Gender Shades-onderzoek uit de video is daar een goed voorbeeld van: de data bestond merendeels uit foto’s van blanke personen. Trainings- en testdatasets die gebruikt worden om de applicatie te laten leren, moeten representatief genoeg zijn voor het doel dat de applicatie beoogt (inclusief data van verschillende bevolkingsgroepen en minderheden). Zo moet worden voorkomen dat de applicatie fouten bevat en discriminerend te werk gaat. Het is dus al nodig om bias te analyseren tijdens het ontwerp van de AI-applicatie. In het [volgende hoofdstuk](https://www.notion.so/2-3-FAIR-data-131105f05af44006b3784262464701e7) gaan we dieper in op eisen aan data.

Alleen de analyse van bias in de trainings- en testdatasets is niet voldoende. We moeten ook kijken naar bias die optreedt tijdens het leerproces van het AI-systeem, dus in de verwerking van de data naar het resultaat van een AI-systeem. Komen er in deze stap nog discriminerende effecten naar boven? Als laatste is het belangrijk dat  het AI-systeem alleen gebruikt wordt door deskundigen die zijn opgeleid om deze applicatie op een verantwoorde en onbevooroordeelde manier toe te passen. Bij de Monocam-applicatie bijvoorbeeld, krijgen alleen agenten de mogelijke overtreders te zien. Het eindoordeel ligt daar nog steeds bij de mens, al is die wel heel goed geholpen door het voorsorteren van vele opnames van voertuigen.

<aside>
🛠️ **Vragen**

1. Kun je aangeven hoe de makers van de Monocam, zoals gepresenteerd in de videoles van de Nationale Politie, ervoor hebben gezorgd dat hun AI-toepassing eerlijk is? Hebben zij bij de gebruikte trainingsdata al rekening hiermee gehouden?
2. Wat zouden de gezichtsherkenningsapplicaties uit het Gender Shades-verhaal moeten doen om ook personen met een donker huidtype beter te leren herkennen? 
3. Waarom is het belangrijk om al tijdens het ontwerp van een AI-toepassing na te denken over fairness?
</aside>

- Antwoorden
    1. De video over de Monocam laat zien dat er heel goed wordt nagedacht over het voorkomen van bias in de trainingsdata. Er zijn criteria opgesteld over wat wel en geen mobiel is. Ook zijn mogelijke criteria uitgesloten omdat die vanwege de wet niet zijn toegestaan. 
    2. De trainingsdataset moet worden uitgebreid met personen met een meer donker huidtype en er moet dus opnieuw worden getraind.
    3. Voorkomen is beter dan genezen. Als voor een applicatie wordt aangetoond dat deze foute eigenschappen heeft, kan dit leiden tot het afdanken van de applicatie en dus tot financieel verlies. Ook kan  ongerustheid in de samenleving ontstaan, waardoor AI in zijn algemeenheid weer in een slechter daglicht komt te staan.

### Accountability

Het principe van accountability vereist dat de verantwoordelijkheid voor beslissingen die door AI-systemen zijn genomen, ligt bij de menselijke ontwikkelaars van de systemen en de gebruikers die de systemen in de praktijk toepassen. Het gaat dan eigenlijk over twee aspecten: de verantwoordingsplicht en de controleerbaarheid. De verantwoordingsplicht zegt iets over de vraag wie verantwoordelijk is voor een uitkomst van zo'n systeem. Controleerbaarheid speelt in  op de vraag hoe ontwikkelaars en gebruikers verantwoordelijk moeten worden gehouden. Als bijvoorbeeld een AI-systeem een antwoord geeft, moeten de verantwoordelijken kunnen uitleggen hoe dit antwoord tot stand is gekomen. Het is belangrijk om de verantwoordelijkheid in alle stadia te bewaken: van systeemontwikkeling, via het moment waarop het systeem wordt toegepast in de praktijk, tot het moment dat het uiteindelijk niet langer gebruikt wordt en verwijderd wordt.

<aside>
🛠️ **Vragen**

1. Op welke manier hebben de makers van de Monocam, de AI-toepassing van de Nationale Politie, ervoor gezorgd dat er is voldaan aan de eisen van verantwoordingsplicht en controleerbaarheid?
</aside>

- Antwoorden
    1. De makers van de Monocam hebben ervoor gezorgd dat er altijd een politiemedewerker naar de geselecteerde foto’s kijkt. Die persoon controleert op juistheid voordat er een bekeuring wordt verstuurd.

### Safety

Het veiligheidsprincipe eist dat, afhankelijk van de praktische setting, het systeem nauwkeurig is en binnen een verwacht foutenpercentage werkt. Een AI-systeem moet betrouwbaar zijn om consistente resultaten te genereren. Het moet veilig zijn en daardoor de privacy en vertrouwelijkheid van gebruikte gegevens waarborgen. Bovendien moet een AI-systeem robuust zijn, om zelfs bij onverwachte veranderingen en verstoringen de werking te garanderen. Stel je bijvoorbeeld eens voor dat de Monocam, zoals gepresenteerd in de videoles van de Nationale Politie, voortdurend foute beslissingen neemt wanneer het harder waait dan windkracht 4.

<aside>
🛠️ **Vragen**

1. Zelfrijdende auto’s hebben al ongelukken veroorzaakt. Welke veiligheidseisen zou jij willen stellen aan het rijdende AI-systeem? Bedenk ook hoe realistisch je eisen zijn. Het is namelijk niet waarschijnlijk dat er in het verkeer nooit meer een ongeluk zal plaatsvinden.
2. Een van de systemen in het Gender Shades-verhaal herkende wel een gezicht in een wit masker, maar niet het gezicht van de donkere dame. Is het veilig als deze AI-systemen maskers herkennen?
</aside>

- Antwoorden
    1. Je zou als eis kunnen stellen dat een zelfrijdende auto minder ongelukken maakt dan de mens in vergelijkbare situaties. Of dat een AI-systeem nooit een fatale fout kan maken die een mens ook nooit zou maken. Ook is het zeker niet gewenst als het systeem onderweg plotseling stopt met werken.
    2. Of dit veilig is of niet, houdt verband met het doel van de applicatie. Als deze gebruikt wordt om iemand te herkennen, is het heel slecht als een persoon die een masker van jouw gezicht draagt, ook wordt herkend als jou. Het kan een minder groot probleem zijn wanneer de applicatie slechts overzichten geeft van de drukte op straat, verdeeld over mannen en vrouwen, om eventuele onrust in te schatten.

### Transparency

Het laatste FAST-principe is transparantie. Beperkte transparantie kan niet alleen de betrouwbaarheid van AI-systemen verminderen, maar ook de validatie van de resultaten en de identificatie van fouten en vooroordelen belemmeren. Daarom is het noodzakelijk om alle gevolgde processen tijdens het ontwerp en het gebruik van een AI-systeem te kunnen beoordelen. Het moet mogelijk zijn om de basisgedachte achter de beslissingen of het gedrag van een systeem te begrijpen. In relatie tot transparantie wordt ook wel gesproken over zogeheten *explainable AI*.  Het doel van explainable AI is om AI-beslissingen transparanter en betrouwbaarder te maken.

Transparantie binnen AI omvat de volgende twee betekenissen:

1. Verklaarbaarheid: de mogelijkheid om te achterhalen hoe een AI-systeem in een bepaalde situatie handelt, en waarom. De logica van de beslissing of het gedrag moet dus begrijpelijk zijn. Dit noemen we ook wel het openen van de ‘black box’ van AI. 
2. Rechtvaardiging: zowel het ontwerp als de inzet van een AI-systeem moet aantoonbaar een rechtvaardiging hebben met betrekking tot deze punten: ethisch toelaatbaar, niet-discriminerend/eerlijk, publiek vertrouwenswaardig en het garanderen van veiligheid.

Om transparantie te bieden moet voor AI-systemen dus eerst het systeem gerechtvaardigd worden. Als het systeem vervolgens is ontwikkeld, moet er voor leken een uitleg komen hoe en waarom een systeem werkt. Als laatste moet er dan weer een rechtvaardiging komen van het gedrag van het AI-systeem. Intenties die aanvankelijk goedbedoeld waren, kunnen namelijk alsnog verkeerd uitpakken.

<aside>
🛠️ **Vragen**

1. Wat betekent de afkorting FAST? Geef in je uitleg Nederlandse begrippen.
2. Transparantie staat niet los van de andere drie principes. Geef aan wat de koppelingen zijn.
3. Verbind de volgende beschrijvingen aan het bijbehorende FAST-principe van AI-ethiek:
    1. De verantwoordelijkheid voor AI-beslissingen ligt bij de menselijke ontwikkelaars en de gebruikers die de systemen in de praktijk toepassen.
    2. Toevoegen van code aan een AI-systeem door onbekende en anonieme programmeurs.
    3. Beperken van bias in datasets door data van verschillende populaties en minderheden op te nemen.
    4. Ervoor zorgen dat een AI-systeem nauwkeurig, betrouwbaar en robuust is.
</aside>

- Antwoorden
    1. De F in FAST staat voor fairness oftewel eerlijkheid. De A staat voor accountability  oftewel verantwoordelijkheid. De S staat voor security oftewel veiligheid. De T staat voor transparency oftewel transparantie/uitlegbaarheid.
    2. Als een AI-systeem transparant is, is duidelijk hoe het systeem omgaat met veiligheid en is het duidelijk dat de applicatie op een eerlijke manier werkt. Waarschijnlijk kan dan ook beter worden beoordeeld wie de verantwoordelijkheid van een AI-systeem draagt.
    3. a) Accountability; b) Transparency, Fairness, Security; c) Fairness; d) Security.

De FAST-principes gaan over het hele AI-systeem. In de volgende paragraaf concentreren we ons op problemen rond de data waarvan AI-systemen afhankelijk zijn.