# Fase 3: Andere dataset gebruiken

In de vorige twee fasen hebben we het bloemen voorbeeld van het voorbeeld in [Image classification with Tensorflow](https://www.tensorflow.org/lite/tutorials/model_maker_image_classification) gebruikt. In deze fase gaan we hetzelfde model gebruiken op een andere dataset. Een dataset met verschillende beroepen.

<aside>
🛠 De volgende stappen moeten worden uitgevoerd:

1. Dataset downloaden
2. Dataset uploaden
3. Dataset uitpakken
4. De stappen uit Fase 1 herhalen.
5. Testen nieuwe app.
</aside>

## Dataset downloaden

![farmer-152.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3c984014-6b2c-4378-9de9-824f138c20aa/farmer-152.jpg)

![waiter-33.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1dda7f08-c884-4a66-abb6-d6bdaf46a60e/waiter-33.jpg)

![mechanic-82.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a17a03d3-2575-4a8a-9d27-d319813feca0/mechanic-82.jpg)

![doctor-101.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c7cc41ab-9d08-46f5-921e-6a85e68c2529/doctor-101.jpg)

- Deze plaatjes zitten in het gecomprimeerde bestand train.tar.gz. Download dit bestand.
    
    [train.tar.gz](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/89e570e6-df2c-4e17-b832-981d858d828a/train.tar.gz)
    
- Pak **train.tar.gz** uit (Met Windows 10 lukt het niet om een tar dan wel gz bestand uit te pakken. Gebruik **[7-Zip](https://www.7-zip.org/download.html)** ). Je krijgt dan een bestand **train.tar**.
- Pak **train.tar** uit. Je krijgt dan een map **train**.

In de map train vind je een aantal mappen met namen van beroepen. In deze mappen met namen van beroepen vind je plaatjes (224x224 pixels) van deze beroepen.

## Dataset uploaden

We gaan de dataset **train.tar.gz** gebruiken om een model te trainen die de beroepen moet gaan herkennen. Dit doen we weer met  [Image classification with Tensorflow](https://www.tensorflow.org/lite/tutorials/model_maker_image_classification).

- Open het [tensorflow notebook](https://www.tensorflow.org/lite/tutorials/model_maker_image_classification)
- Klik op: **Run in Google Colab** en ga weer naar de nieuw geopende tab
- Klik op het mapje icon aan de linker kant en het pijtje naar boven. Je ziet nu welke mappen er op de server voor jou beschikbaar zijn. Open **..**  , zoek vervolgens naar de **/tmp** map en ga hier op staan.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/642681db-d779-47d6-8f5d-417039ff0295/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/642681db-d779-47d6-8f5d-417039ff0295/Untitled.png)

- Klik de rechter muis knop en selecteer **Upload**. Upload vervolgens van je laptop of PC het bestand **train.tar.gz**. Je kunt nu gerust even pauze nemen want dit duur mogelijk een tijdje.

Je ziet nu het bestand **train.tar.gz** in de **/tmp** map verschijnen. 

- Maak vervolgens in de map **/tmp** een map **train** aan om de data van de dataset in te zetten door op de rechter muis knop te klikken en  **New Folder** te selecteren.

Als alles correct gegaan is zie je het volgende:

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6507e4ab-f358-42e1-ab5e-cd427c3f061a/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6507e4ab-f358-42e1-ab5e-cd427c3f061a/Untitled.png)

## Dataset uitpakken

- Ga nu in het notebook staan in de eerste cel in de sectie "**Prerequisites**" die begint met: **!pip** en selecteer in het menu bovenaan: "**+ Code**".

Je krijgt nu een nieuwe cel.

- Zet in de nieuwe cel de volgende commando's
    
    ```bash
    !tar xvf /tmp/train.tar.gz -C /tmp/train
    !rm /tmp/train/*/Thumbs.db
    ```
    
    Het eerste commando pakt de dataset uit in de map **/tmp/train**.
    
    Het tweede commando zorgt ervoor dat bepaalde ongewenste bestanden verwijderd worden
    
- Voer de code cel vervolgens uit door op het pijltje te gaan staan en de linker muis knop te klikken. Je ziet nu dat de dataset wordt uitgepakt in de map **/tmp/train**.

## Stappen uit Fase 1 herhalen

- Voer alle andere cellen in de sectie "**Prerequisites**" uit.
- Scroll naar beneden naar de code cel in de sectie "**Get the data path**" die begint met: **image_path** en pas deze code cel aan zodat deze er als volgt uitziet:
    
    ```python
    image_path = tf.keras.utils.get_file('/tmp/train','/tmp/train')
    image_path = os.path.join(os.path.dirname(image_path),'train')
    ```
    
- Voer vervolgens deze cel uit.
- Voer nu weer net als in Fase 1 de cellen uit in de sectie **"Run the example**".

De cel model.export(export_dir='.') heeft het model  **model.tflite** geplaatst in de map **/content**.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dc3e7ace-5eec-4e57-847f-758a06ad499b/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dc3e7ace-5eec-4e57-847f-758a06ad499b/Untitled.png)

### Maken App met het nieuwe model

Nu we weer een getraind model hebben kunnen we deze op dezelfde manier in een app verwerken zoals in Fase 1 is uitgelegd.

- Download **model.tflite** en hernoem die naar **beroepen.tflite** en bouw hiermee een nieuwe app.

## Testen nieuwe app

Je kunt je App testen door de plaatjes van de dataset **train.tar.gz** die je op je laptop of PC gedownload hebt op het scherm te openen en je telefoon erbij te houden om te testen hoe goed de App plaatjes van bepaalde beroepen herkent. Je kunt natuurlijk ook op het internet naar plaatjes zoeken die bij deze beroepen horen en kijken of die worden herkend.