# In de praktijk
Tegenwoordig zie je op steeds meer plekken kunstmatige intelligentie terug komen. Er zijn tal van fantastische voorbeelden die je misschien wel eens tegen bent gekomen, en elk jaar komen er tientallen nieuwe plekken bij! We zullen gaan kijken naar een klein aantal bekende en recente implementaties van KI.

## AlphaGo

In hoofdstuk [1.2. Geschiedenis en toekomst](https://www.notion.so/1-2-Geschiedenis-en-toekomst-4bd92d94b5a9457c985a58eba4ba14b1) hebben we gelezen over de doorbraak van DeepMind's AlphaGo, een KI die gespecialiseerd is in het spelen van het gelijknamige spel Go. AlphaGo wist in 2015 voor het eerst de beste speler ter wereld te verslaan in een spelletje.

Het spel heeft enorm veel mogelijke zetten, waardoor het niet mogelijk is voor simpelere algoritmes om dit probleem op te lossen.

![AlphaGo die een spel speelt tegen Lee Sedol](https://live.staticflickr.com/1626/25708381781_eee5664c65_c.jpg)

AlphaGo die een spel speelt tegen Lee Sedol

### Technieken

AlphaGo maakt gebruik van een combinatie tussen [*Monte Carlo Tree Search*](https://en.wikipedia.org/wiki/Monte_Carlo_tree_search) (MCTS) en deep learning [*neurale netwerken*](https://www.notion.so/3-5-Neurale-netwerken-4778ac2fbe494b9cbe50001b3d19d1c9). Monte Carlo Tree search is een techniek die gebruik wordt om zo goed mogelijk te zoeken naar een oplossing. Het maakt hiervoor gebruik van heuristieken, zoals bijvoorbeeld ook gedaan wordt bij het [zoekalgoritme A*](https://www.educative.io/edpresso/what-is-the-a-star-algorithm).

*Deep learning* betekent dat er meerdere "lagen" aan neuronen in het neurale netwerk aanwezig zijn. Over het algemeen zijn veel toepasbare vormen van *deep neural networks*. 

### Toepassingen

MCTS wordt toegepast om computers bord en videospellen te laten spelen. Zo is er door middel van MCTS een bot gemaakt voor bijvoorbeeld schaken, kolonisten van Catan, Ms. Pac-Man, Poker, Fable Legends, etc. Het wordt ook daadwerkelijk gebruikt in het spel TOTAL WAR: ROME II om de speler het zo moeilijk mogelijk te maken.

Daarnaast wordt het ook gebruikt door de [autopiloot in Tesla](https://youtu.be/j0z4FweCy4M?t=4929) auto's om beslissingen te maken.

Deep learning is enorm breed en wordt in veel gebieden toegepast. Zoals Financial fraud detection, Medical image analysis, Drug discovery and toxicology, Natural language processing, Image recognition en nog veel andere velden.

Je kunt hier later meer over leren in [3.5. Neurale netwerken](https://www.notion.so/3-5-Neurale-netwerken-4778ac2fbe494b9cbe50001b3d19d1c9).

## Tay de Twitter bot

Microsoft heeft in 2016 een twitterbot gemaakt met KI technieken. De bot leerde door middel van de tweets van andere twitter gebruikers. Hoewel het idee erg leuk was, ging dit compleet fout. Binnen de kortste keren begon de bot onder andere racistische en seksistische opmerkingen te maken. Nadat Microsoft hierachter kwam, hebben ze snel de bot offline gehaald. Volgens Microsoft was het probleem dat "internet trollen" massaal misbruik maakte van de KI, waardoor deze de door hen gestuurde opmerkingen ging herhalen.

![Hier kan je zien hoe de tweets van Tay binnen een dag veranderden: van vriendelijk, naar hatelijk.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/03be44ae-253c-48a3-ae37-b9b2472d8977/CeSpN5oWAAEIu_o.jpg)

Hier kan je zien hoe de tweets van Tay binnen een dag veranderden: van vriendelijk, naar hatelijk.

### Technieken

Om teksten te kunnen genereren en lezen, moet een systeem taal begrijpen. Hoewel dit voor een mens over het algemeen niet heel lastig is, is het voor een computer nog aardig moeilijk om taal écht te snappen. De overkoepelende term voor het verwerken en schrijven van taal in informatica is [*Natural Language Processing*](https://en.wikipedia.org/wiki/Natural_language_processing) (*NLP*), of in het Nederlands *Natuurlijke Taalverwerking*. NLP wordt tegenwoordig veel gedaan door middel van neurale netwerken. Vroeger werden statistische modellen gebruikt om deze taak uit te voeren, deze zijn bijna compleet overbodig geworden.

Microsoft zal een vorm van *Reinforcement Learning* gebruikt hebben, om te kunnen leren van de communicatie met gebruikers. Bij reinforcement learning moet de KI zelf beredeneren of een actie goed of slecht was. Dat kan bijvoorbeeld door positieve of negatieve feedback op een actie. Als de KI iets doet wat de gebruiker waardeert, zal de KI leren om dit vaker te doen. Indien de gebruiker het niet waardeert, zal het minder vaak zo reageren.

### Toepassingen

NLP wordt enorm veel gebruikt, elke keer als je met een chatbot praat (bij een online webshop of ergens anders) dan wordt er gebruik gemaakt van NLP. 

Hele bekende voorbeelden die enorm veel gebruik moeten maken van NLP zijn Google Now, Siri en Alexa, de spraakassistenten van Google, Apple en Amazon. Deze systemen moeten onder andere gebruik maken van NLP om spraak naar tekst om te zetten, tekst te begrijpen en een tekst weer uit te kunnen spreken.

Je kunt hier later meer over leren in ‣.

## GAN

Heel veel bekende vormen van KI maken gebruik van GANs, *Generative Adversarial Networks*. Netwerken die hier gebruik van maken zijn enorm goed in het creëren van data, die lijkt op de getrainde data. Je kan het zien alsof je een vriend een incomplete puzzel geeft, waar 10 puzzelstukjes van missen. Maar wonder boven wonder kan je vriend de missende puzzelstukjes zelf bedenken en tekenen!

Deze slimme systemen bestaan uit twee onderdelen: een generator en een discriminator. De generator moet zorgen dat het data weet te maken wat de discriminator niet kan onderscheiden van echte data. De discriminator moet op haar beurt leren om zo goed mogelijk de neppe van de echte data te onderscheiden.

Je kan het vergelijken met valsemunters (generator) en de politie (discriminator). De Europese bank stopt allemaal verschillende beveiligingskenmerken in de Euro, zodat de politie het echte geld kan onderscheiden van het nepgeld. De illegale drukkers proberen al die verschillende kenmerken te imiteren, zodat het heel lastig wordt om het neppe geld te onderscheiden van echt geld. De politie moet steeds beter gaan kijken of het geld nep of echt is, waarna de gelddrukkers nóg beter illegaal geld gaan drukken. Dit is een wedloop die voort blijft gaan.

### Toepassingen

Deze netwerken zijn helemaal "hot and happening", maar waar kunnen ze voor gebruikt worden in de echte wereld?

#### **Medisch**

In de medische wereld worden sinds kort ook dergelijke systemen gebruikt voor de bestrijding van ziektes als kanker. Het netwerk wordt gebruikt om moleculaire structuren te genereren, die gebruikt kunnen worden in medicijnen tegen ziektes. 

#### **Beeldmateriaal**

GANs kunnen ook gebruikt worden om oude foto's of films te "restaureren". De KI wordt gevoerd met een verouderde zwart-wit foto of video en het genereert een foto of video van hoge kwaliteit. Op deze manier kunnen we een ongekende blik in het verleden krijgen. 

Het kan ook gebruikt worden om bijvoorbeeld games op een hoge resolutie te spelen. Tegenwoordig heb je 4K en zelfs 8K schermen, een 8K scherm heeft meer dan 33 miljoen pixels! Om deze allemaal aan te kunnen sturen is veel rekenkracht nodig, soms te veel. Om het mogelijk te maken om toch al die pixels aan te sturen terwijl je een spelletje speelt, kan een KI de resolutie verhogen. Jouw computer maakt dus een plaatje van bijvoorbeeld 2 miljoen pixels waarna de KI er 31 miljoen bij bedenkt!

In de toekomst zullen we veel meer toepassingen gaan zien van GANs. Omdat het een relatief nieuwe KI is, zijn er nog veel velden onderbelicht en onontdekt. 

#### **Deepfakes**

Deepfakes zijn sinds de laatste jaren steeds populairder en makkelijker om te maken. Zo maken veel apps gebruik van "filters" gebaseerd op de techniek. Deepfakes kunnen erg grappig zijn, maar ze kunnen ook veel schade aanrichten. Zo kunnen kwaadwillenden interviews of statements van bekende personen of politici namaken. Deze filmpjes zijn door het blote oog niet makkelijk te onderscheiden van *echte* interviews. 

[https://www.youtube.com/watch?v=gNYkspmq5e0](https://www.youtube.com/watch?v=gNYkspmq5e0)

[https://www.youtube.com/watch?v=IvY-Abd2FfM](https://www.youtube.com/watch?v=IvY-Abd2FfM)

De 47 minuten durende, maar zeer interessante, documentaire  “[Zien is geloven](https://www.npostart.nl/vpro-tegenlicht/07-03-2021/VPWON_1322213)” van VPRO tegenlicht geeft goed inzicht in de problemen rond Deep Fakes maar laat ook zien dat er goede dingen mee kunnen worden gedaan.

<aside>
🛠 **Opdracht**

Zoek zelf nog een aansprekend Deepfake videofragment.

</aside>

#### **Muzikale AI**

De onderzoekers van OpenAI hebben [GANs](https://openai.com/blog/jukebox/) gebruikt om een [kunstmatige intelligentie muziek](https://openai.com/blog/jukebox/) te laten maken. Of beter gezegd, de KI moet bekende liedjes afmaken. Het systeem krijgt het begin van een liedje te *horen*, waarna het zelf moet bedenken hoe het liedje verder zal gaan. De uitkomsten zijn vaak erg bizar en klinken totaal anders dan je zou verwachten.

[Pop, in the style of Rick Astley - Jukebox by OpenAI](https://soundcloud.com/openai_audio/jukebox-914891098)

[All Star, but an AI continues the song [OpenAI Jukebox]](https://www.youtube.com/watch?v=8sFXsP71wfA)

<aside>
🛠 **Opdracht**

Luister naar de nummers. Zijn de teksten die worden gegenereerd enigszins realistisch?

</aside>

#### **Foto's maken**

Een GAN kan ook foto's generen aan de hand van simplistische tekeningen. Deze technieken laten de gebruiker een simpel plaatje tekenen van bijvoorbeeld een kat, waarna deze gegenereerd wordt op een zo realistisch mogelijke manier.

[https://slo-ai.github.io/pix2pix/](https://slo-ai.github.io/pix2pix/)

<aside>
🛠  **Opdracht**

Probeer zelf een in bovenstaande applet een aantal eigen tekeningen (minimaal 5 voor één categorie) naar een foto om te zetten. Maak screenshots van je pogingen  en geef ze een cijfer van 1 tot 10 voor de mate van realisme .

</aside>

[NVIDIA](https://www.nvidia.com/en-us/studio/canvas/) heeft deze techniek ook toegepast op landschappen. Het systeem genereert een realistisch ogend landschap gebasseerd op een abstracte tekening van een landschap. De kleuren op het plaatje betekenen allemaal iets anders, elke kleur staat voor een bepaald materiaal. Zo wordt grijs vertaald naar wolken, lichtblauw naar zee, bordeaux rood naar bloemen, etc.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/182a113b-ec1b-429a-bd23-be5edfa336c2/gaugan_input.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/182a113b-ec1b-429a-bd23-be5edfa336c2/gaugan_input.png)

#### Deze persoon bestaat niet(!)

Onderzoekers hebben in december 2019 een paper uitgebracht over *StyleGAN2*, een netwerk dat mensen en objecten kan genereren die nooit bestaan hebben. Om te laten zien hoe goed hun netwerk is, hebben ze een website gemaakt: [https://thispersondoesnotexist.com](https://thispersondoesnotexist.com).

Op de website wordt groot een foto van een persoon getoond, maar de grap is dat deze persoon niet bestaat en compleet is gegenereerd door de GAN. 

[https://thispersondoesnotexist.com/](https://thispersondoesnotexist.com/)

<aside>
🛠 **Opdracht**

Ga naar de website en bekijk de personen. De website laat een nieuwe foto zien als je de pagina herlaadt (F5). Kan jij de foto's van echt onderscheiden? Zo ja, hoe? Zo niet, waarom niet?

</aside>

- Antwoord
    
    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/10b442ce-49de-49df-9177-008117a8f203/5_example.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/10b442ce-49de-49df-9177-008117a8f203/5_example.png)
    
    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/11dbd4de-b03c-4598-95b2-82df3e15d931/3_example.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/11dbd4de-b03c-4598-95b2-82df3e15d931/3_example.png)
    
    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/80d75380-cfb1-463f-b9b7-5e0c34bdce58/7_example.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/80d75380-cfb1-463f-b9b7-5e0c34bdce58/7_example.png)
    
    Misschien vond je het erg lastig, of had je het snel door als je goed keek naar het plaatje. Vaak kan je bij overgangen van personen naar objecten/achtergrond nog wel eens een "artifact" vinden. Haar, ogen en kleding kunnen ook nog wel eens fout gaan. Als je heel ver in de plaatjes inzoomt kan je ook soms wel zien dat het een beetje raar oogt.
    
    Ook kan het gebeuren dat het netwerk een object een beetje half heeft gegenereerd. Hierdoor is het voor een deel zichtbaar of doorzichtig. Een beetje een geest-achtig effect geeft dit.
    

<aside>
🛠 **Vragen**

1. Wat is Monte Carlo Tree search?
2. Wat is de overkoepelende term voor het verwerken en schrijven van taal in informatica?
3. Leg uit wat een GAN is en noem 2 serieuze toepassingen waarin GAN's worden gebruikt.
</aside>

- Antwoorden