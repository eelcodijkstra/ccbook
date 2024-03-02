# Fase 2: Optimaliseren Neuraal Netwerk

## Optimaliseren neural netwerk

In *Fase1* hebben we een neuraal netwerk gemaakt om bloemen te herkennen. In deze *Fase* bestudeer je hoe je een dergelijk neuraal netwerk kunt optimaliseren zodat het zo goed mogelijk werkt.

## Competitie

We gaan werken in groepjes van drie leerlingen. Maak daarom eerst groepjes en ga daarna verder. Aan het eind van *Fase2* doen we een competitie met de in Fase 1 gemaakte verschillende apps en die op de verschillende telefoons staan. Als alle apps met slechts één export zijn gebouwd is iedere app gelijk en is de competitie zinloos. Heeft ieder groepje zelf het netwerk getraind dan gaan we in de competitie als volgt te werk. 

- Download op één computer de foto's waarmee de netwerken zijn getraind:
[https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz](https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz)
- Pak dit bestand uit zodat we mappen met foto's van bloemen krijgen.
- Elk groepje mag uit elke map een zelfde aantal foto's kiezen. De gekozen foto's worden in een testmap gezet. Open de fotobestanden op de computer en scan met de apps op de mobiele telefoons de foto's.
- Alternatief: Elke groep zoekt een plaatjes op het internet van daisies (madeliefjes), dandelions (paardebloemen), roses (rozen), sunflowers (zonnebloemen) en tulips (tulpen) en plaats die in een testmap

Elk groepje test de App met alle foto's uit de test map of alle op het internet gekozen afbeeldingen en telt de percentages op waarmee de App de bloemen goed herkent. Als de App een bloem fout herkent is het percentage 0. De groep met de hoogste score wint.

## Hoe kun je een neural netwerk optimaliseren

Je kunt het neurale netwerk optimaliseren door een ander pad in het notebook van de vorige keer te kiezen.

- Ga weer met [deze link](https://www.tensorflow.org/lite/tutorials/model_maker_image_classification)  naar de Google Colab tutorial voor het classificeren van beelden
- Klik weer op **Run in Google Colab** en ga naar het nieuw geopende tabblad.
- Voer all cellen in de sectie **Prerequisites** uit (2 cellen) om de juiste libraries te importeren
- Ga nu naar de sectie "**Detailed Process**" en voer de cellen uit in **Step 1: Load Input Data Specific to an On-device ML App**

In **Step 2: Customize the TensorFlow Model** wordt eerst met het zelfde model als je hebt gebruikt in Fase 1 getraind met training data en validatie data. In **Step 3: Evaluate the Customized Model** wordt vervolgens gekeken hoe goed de test data wordt geclassificeerd. We gaan nu eerst een aantal keer trainen met hetzelfde model en slaan het resultaat op in verschillende mappen, zodat je straks de beste kan gebruiken in je app.

- Maak eerst een aantal nieuwe mappen aan waar je straks het model naar kunt exporteren. Een nieuwe map maak je door in het bestanden gedeelte met je rechter muisknop te klikken en vervolgens op "nieuwe map te klikken". In de figuur hieronder is de map **run1** aangemaakt.

![Extramap.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ccd8cc65-90a5-4a9c-99d5-083abc97f9f5/Extramap.jpg)

- Voer "**Step 2**" en "**Step 3**" uit.   Noteer de resultaten **loss** en **accuracy** van zowel de laatste training stap van de uitvoer van de eerste cel in "**Step 2**" en van de uitvoer van de eerste cel in "**Step 3**" Hoe kleiner de loss en hoe hoger de accuracy hoe beter het resultaat. Na iedere herhaling exporteer je het model naar een nieuwe map door de eerste cel in "**Step 4**" aan te passen. (b.v. naar **model.export(export_dir='./run1')**  als je de map **run1** hebt aangemaakt) Herhaal de stappen "**Step 2**" , "**Step 3**" en "**Step 4**" een aantal keer (b.v 3 keer).
- Zijn er veel verschillen?

In de sectie "**Change the model**" zijn er een aantal suggesties ter verbetering.

- Probeer een aantal van deze suggesties uit en exporteer de modellen weer naar nieuwe mappen. Gebruik wel steeds de zelfde training , validatie en test data. Vergeet niet iedere keer te exporteren.
- B.v. in de sectie "**Change to the model that's supported in this library**" kun je eens kijken wat het effect op loss en accuracy is van de modellen:
'efficientnet_lite0', 'efficientnet_lite1', 'efficientnet_lite2', 'efficientnet_lite3', 'efficientnet_lite4', 'mobilenet_v2', 'resnet_50'. Hoeveel parameters zitten in jouw gebruikte modellen?
- En in de sectie "**Change to the model in TensorFlow Hub**" kun je ook nog een geheel ander model inladen namelijk [**Inception V3](https://tfhub.dev/google/imagenet/inception_v3/feature_vector/1).**  Voer de stappen uit en kijk of het model beter voorspeld. Hoeveel parameters zitten in dit model?
- Als laatste, behalve het herhalen van de training kun je ook proberen het model te verbeteren. Je ziet dat er nu 5 trainingsronden worden uitgevoerd. Je kunt deze verhogen door de epochs waarde in te stellen (b.v. epochs=7).
- Maak een app met het model met de beste **loss** en **accuracy.**

Haalt de nieuwe app een hogere score met de afbeeldingen uit de competitie?