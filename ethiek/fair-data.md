(ethiek-fair-data)=
# FAIR data

## De principes van FAIR data

Naast de FAST-principes wordt vaak nog een afkorting gebruikt die specifiek gericht is op het gebruik van data: FAIR data. FAIR data omvat data die voldoet aan principes van vindbaarheid (*findability*), toegankelijkheid (*accessibility*), interoperabiliteit (*interoperability*) en herbruikbaarheid (*reusability)*. In eerste instantie gaat het daarbij om wetenschappelijke data. Daarbij ligt de nadruk op machine-actionability: het vermogen van computersystemen om gegevens te vinden, toegang te krijgen, samen te werken en te hergebruiken zonder of met minimale menselijke tussenkomst. De vier principes van FAIR data zijn elk weer onderverdeeld in een aantal uitgangspunten:

![FAIR data.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/10eaf5da-5976-4d04-bdb9-591b28e35f42/FAIR_data.png)

### Vindbaarheid (findability)

Vindbaarheid van data gaat over het principe dat metadata en data gemakkelijk vindbaar moeten zijn, voor zowel mensen als computers. Metadata omvat gegevens die de karakteristieken van bepaalde gegevens beschrijven: data over data. Goede metadata is essentieel voor automatische detectie van datasets en services. Stel je eens voor dat een data scientist van een winkelketen een analyse wil maken van de klantdata om te ontdekken hoe vaste klanten vaker een specifieke, geïndividualiseerde aanbieding kunnen krijgen. Helaas kan zij  in het databestand met klantgegevens eigenlijk niet goed identificeren wat nou de aankopen van klanten zijn. Dan wordt zo’n onderzoek moeilijk. Wanneer vooraf, bij het ontwerpen van de klantdataset, duidelijk in de metadata was aangegeven wat aankopen zijn, zou dat veel extra werk hebben gescheeld.

<aside>
🛠️ **Vraag**

1. Welke van de volgende gegevens zou je als metadata mogen beschouwen?
    1. Het bestandsformaat van een databestand.
    2. De naam van een databestand.
    3. Het moment van creatie van een databestand.
    4. De naam van een klant in een databestand met klantaankopen.
2. Bekijk de volgende tabel over het VO-onderwijs in Nederland:
    
    [CBS Statline](https://opendata.cbs.nl/statline/#/CBS/nl/dataset/80041ned/table?ts=1640693574043)
    
    1. Geef de metadata over geslacht, migratieachtergrond en havo leerjaar 3-5.
    2. Wat zijn de bronnen waarop deze tabel is gebaseerd?
</aside>

- Antwoord
    1. a, b en c zijn metadata, d niet.
    2. Om deze metadata te vinden beweeg je je muis over de kolomtitels of druk je op de knop I.
        1. Geslacht: inclusief leerlingen van wie het geslacht onbekend is.
        Migratieachtergrond: kenmerk dat weergeeft met welk land een persoon verbonden is op basis van het geboorteland van de ouders of van zichzelf; inclusief deelnemers met een onbekende migratieachtergrond.
        Havo leerjaar 3-5: hoger algemeen voortgezet onderwijs (havo), inclusief Engelse Stroom.
        2. Gebruikte databron(nen):
        -  Schooljaren 2003/4 tot en met 2004/5: Onderwijsnummerbestand Voortgezet Onderwijs (BRON-vo), Dienst Uitvoering Onderwijs (DUO)/CBS én leerlingtellingen vmbo
           landbouwonderwijs, Ministerie van Economische Zaken
        -  Schooljaar 2005/6: Onderwijsnummerbestand Voortgezet Onderwijs (BRON-vo), Dienst Uitvoering Onderwijs (DUO)/CBS
        -  Vanaf 2006/7: Eéncijferbestand Voortgezet Onderwijs, Dienst Uitvoering Onderwijs (DUO)/CBS
        -  Stelsel van Sociaal-statistische Bestanden (SSB), CBS.
            
            ```
            
            ```
            

### Toegankelijkheid (accessibility)

Wanneer een gebruiker data heeft gevonden, wordt het belangrijk hoe die data kunnen worden geraadpleegd, eventueel inclusief authenticatie en autorisatie ervan. Bedenk maar eens  hoe moeilijk het wordt om de klantaankopen uit het bovenstaande voorbeeld in de volgende situatie te analyseren: het bestand is beveiligd met een wachtwoord dat alleen bekend is bij een medewerker van een ICT-bedrijf dat al twee jaar geen diensten meer aan de winkelketen levert.

<aside>
🛠️ **Vraag**

1. Welke voorbeelden in de onderstaande lijst zijn goede voorbeelden van data accessibility?
    1. Het bouwen van een dashboard dat gegevens uit verschillende tabellen van een database haalt, kan alleen worden voltooid door een teamlid dat weet hoe een database te doorzoeken met behulp van SQL of een andere gespecialiseerde querytaal.
    2. Het bouwen van een dashboard dat gegevens uit verschillende tabellen van een database haalt, kan alleen worden voltooid wanneer er formele toestemming is van de eigenaar van de data om die te mogen gebruiken.
    3. Het bouwen van een dashboard dat gegevens uit verschillende tabellen van een database haalt, kan alleen worden voltooid wanneer alle data is geprogrammeerd in dezelfde programmeertaal.
2. Een van de bronnen waarop de tabel over het VO-onderwijs in Nederland is gebaseerd, is het Eéncijferbestand Voortgezet Onderwijs, Dienst Uitvoering Onderwijs (DUO)/CBS. Een korte zoektocht op internet brengt je naar de [open data site van DUO](https://duo.nl/open_onderwijsdata/).
    1. Doe deze zoektocht ook zelf.
    2. Ga op de site van DUO op zoek naar het aantal leerlingen op jouw school in de afdeling waar je nu zit in het vorige schooljaar (bijvoorbeeld havo lj 4-5 Natuur en Techniek,  of vwo lj 4-6 Natuur en Gezondheid).
    3. In welke mate voldoet de gevonden data aan vindbaarheid en toegankelijkheid?
    4. Vind je in dit bestand alle informatie die nodig is om de CBS-tabel te vormen?
</aside>

- Antwoord
    1. a en b zijn goede voorbeelden van data accessibility; c is geen goed voorbeeld van data accessibility, maar gaat over interoperabiliteit.
    2. b) Binnen open data kies je voor Databestanden **→** Voortgezet onderwijs → Leerlingen → Leerlingen per vestiging naar onderwijstype, sector, afdeling, opleiding. Kies daar het bovenste Excel-bestand en ga op zoek naar de gegevens van jouw school.
    c) Vanuit de CBS-tabel was er niet direct een link naar de data, wat de vindbaarheid bemoeilijkt. De toegankelijkheid bij zowel het CBS als DUO is open, er is geen authenticatie en autorisatie aanwezig.
    d) Er zijn geen gegevens over migratieachtergrond aanwezig. 

### Interoperabiliteit (interoperability)

Je moet data samen met andere data kunnen gebruiken. Gegevens moeten dus geschikt zijn voor het samenwerken met applicaties of workflows voor analyse, opslag en verwerking. Om dat mogelijk te maken, moet data gebruikmaken van een formele, toegankelijke, gedeelde en breed toepasbare taal voor kennisrepresentatie. Stel je eens voor dat het programma waarmee het databestand met klantaankopen kan worden uitgelezen, ook nog eens geprogrammeerd is in een taal die niemand anders dan medewerkers van het oorspronkelijke ICT-bedrijf, nog kan lezen en schrijven.

<aside>
🛠️ **Vraag**

1. Welke voorbeelden in de onderstaande lijst zijn goede voorbeelden van interoperabiliteit van data?
    1. De interne data-architectuur van een ziekenhuis en een huisartsenpraktijk is goed ingericht, waardoor deze twee zelfstandig opererende organisaties goed kunnen samenwerken.
    2. Een dierenartsenpraktijk heeft haar hrm-data zo ingericht dat zij zonder problemen data over medewerkers kan delen met een huisartsenpraktijk.
    3. De bedrijfsprocessen van een metaalfabriek en een toeleveringsbedrijf zijn zo op elkaar afgestemd dat zij onderling zonder problemen data over het productieproces kunnen delen.
2. Je hebt het databestand bij DUO opgehaald. Daar staat niets in over de migratieachtergrond. Die informatie staat waarschijnlijk in de bron [Stelsel van Sociaal-statistische Bestanden](https://www.cbs.nl/nl-nl/onze-diensten/methoden/onderzoeksomschrijvingen/korte-onderzoeksbeschrijvingen/stelsel-van-sociaal-statistische-bestanden--ssb--).
    1. Wat is er minimaal nodig om deze koppeling te maken?
    2. Waarom zul je als buitenstaander niet alle gegevens over een leerling kunnen vinden?
    3. Zou je toegang tot de individuele gegevens kunnen krijgen?
</aside>

- Antwoord
    1. a en c zijn goede voorbeelden van interoperabiliteit; bijvoorbeeld overdracht van gegevens van patiënten in a gaat dan goed, en bij c kan het toeleveringsbedrijf het voorraadbeheer afstemmen op de voorraad van de fabriek. 
    b is geen goed voorbeeld omdat het delen van hrm-data van medewerkers in dit geval niet noodzakelijk (en wellicht zelfs niet wenselijk) is.
    2. In de tabel bij het CBS is er een uitsplitsing op migratieachtergrond aanwezig.
        1. Dus óf er moet een uitsplitsing aanwezig zijn per school naar migratieachtergrond in de DUO-bestanden, óf het CBS moet toegang hebben tot alle gegevens van alle leerlingen via DUO en van alle leerlingen via de bron [Stelsel van Sociaal-statistische Bestanden](https://www.cbs.nl/nl-nl/onze-diensten/methoden/onderzoeksomschrijvingen/korte-onderzoeksbeschrijvingen/stelsel-van-sociaal-statistische-bestanden--ssb--) waaruit de migratieachtergrond wordt geleverd. Voor geautomatiseerde verwerking is het dus nodig dat de data van deze bestanden overeenkomstige metadata heeft.
        2. Vanwege privacywetgeving mag niet iedereen individuele gegevens bekijken.
        3. In het [privacystatemen](https://www.cbs.nl/nl-nl/over-ons/organisatie/privacy)t van het CBS staat onder meer:
        ”*Het CBS gebruikt de gegevens alléén voor statistisch en wetenschappelijk doel. Gebruik voor fiscale, administratieve, controle en gerechtelijke doeleinden is wettelijk uitgesloten. Ook gebruiken we de gegevens niet voor marketing.”*
        en 
        ”*Ook worden persoonsgegevens verwerkt bij [wetenschappelijke studies van derden](https://www.cbs.nl/nl-nl/onze-diensten/maatwerk-en-microdata/microdata-zelf-onderzoek-doen/publicaties).”*
        Geautoriseerde medewerkers en geautoriseerde onderzoekers kunnen dus toegang krijgen tot individuele gegevens.

### Herbruikbaarheid (reusability)

Het laatste principe van FAIR data gaat over de (her)bruikbaarheid van data. Data en metadata moeten goed worden beschreven met meerdere relevante attributen, zodat de herbruikbaarheid ervan optimaal is. Op die manier is data in verschillende omstandigheden en systemen mogelijk. Kijk maar eens naar het eerdere voorbeeld van de klantaankopen. Stel je voor dat een andere data scientist een jaar later de klantaankopen wil hergebruiken in een ander onderzoek. Het zou dan goed zijn wanneer de informatie over het bestand (de metadata) inmiddels is bijgewerkt, zodat de problemen van een jaar eerder niet opnieuw optreden.

<aside>
🛠️ **Vraag**

1. De overheid verzamelt van oudsher op reguliere basis data over personen, bedrijven, instellingen, markten, wegen, natuur, emissies, woningen et cetera. We noemen dit publieke data. Het CBS is daarin een belangrijke organisatie. Welke van de volgende beweringen over het belang van hergebruik van publieke data zijn juist? 
    1. Voor wetenschappers is publieke data van waarde, omdat ze vaak een grote populatie en/of een lang tijdsbestek bestrijkt en niemand doorgaans buiten de populatie van overheidsadministraties valt.
    2. Voor bedrijven is publieke data belangrijk, omdat ze daarmee een betrouwbare database van potentiële klanten voor hun producten en diensten kunnen opbouwen. Iedereen ‘zit’ immers in die publieke data.
    3. Voor overheden is publieke data een potentiële bron van kennis. Deze kennis werpt licht op het effect van hun beleid en helpt ze om complexe taken uit te voeren. Zo’n complexe taak is bijvoorbeeld het bewaken van waarden als veiligheid, privacy, zelfbeschikking, solidariteit en eerlijke concurrentie.
</aside>

- Antwoord
    1. a en c zijn goede redenen waarom hergebruik van publieke data belangrijk is. b is een slecht voorbeeld, omdat publieke data geen persoonsgegevens bevat die bedrijven kunnen en mogen gebruiken.

We zijn aan het einde gekomen van de introductie van de ethische principes waaraan AI-systemen, en meer algemeen systemen die zijn gebaseerd op persoonlijke gegevens, zouden moeten voldoen. Dat niet alle systemen aan deze principes beantwoorden, is een zorg voor de samenleving en dus ook voor de politiek. Het is niet altijd makkelijk om aan alle principes te voldoen. In de verdieping [Ethiek en AI](https://www.notion.so/E-Ethiek-en-AI-040d6779dbd947afa6ca13872c54245b) kun je zelf aan de slag gaan met het analyseren van AI-systemen in relatie tot de principes FAST en FAIR.