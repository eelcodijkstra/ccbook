# Fase 4: Eigen dataset gebruiken

Nog leuker kan het worden als jullie een eigen dataset gebruiken. In Fase 3 heb je gezien dat er heel veel afbeeldingen per categorie aanwezig zijn. Het zal een hele klus worden om een behoorlijk aantal afbeeldingen bij elkaar te verzamelen en deze ook nog naar een juiste formaat te transformeren. Dat doe je natuurlijk niet alleen.

<aside>
🛠 De volgende stappen moeten worden uitgevoerd:

1. Thema en klassen verzinnen
2. Afbeeldingen verzamelen
3. Dataset inpakken
4. De stappen uit Fase 3 herhalen.
</aside>

## Thema en klassen verzinnen

- Verzin gezamenlijk een thema met daarin een aantal klassen.
b.v. het thema **muziek** met daarin de klassen blues, house, punk, reggae en soul.

## Afbeeldingen verzamelen

- Verdeel de leerlingen over de klassen en verzamel per leerling afbeeldingen voor de jouw aangewezen klasse op b.v. een usb-stick of in een eigen map op je computer.
- Als het mogelijk is om een voor iedereen toegankelijke map **muziek** aan maken met daarin de sub mappen blues, house, punk, reggae en soul. Dan kan iedere leerling zijn verzameling in die map plaatsen. Lukt dat niet laat dan een usb-stick rondgaan met de zelfde structuur en laat iedereen zijn verzameling op die stick plaatsen. De map ziet er dan bijv. als volgt uit:
    
    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3cae1ef6-0d16-4713-8c77-6800840cecbb/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3cae1ef6-0d16-4713-8c77-6800840cecbb/Untitled.png)
    

## Inpakken eigen dataset

Als er voldoende plaatjes in de sub mappen staan kun je het geheel inpakken als een data set. Het is belangrijk dat je eerst een **tar** bestand maakt zodat je bijv. een bestand **muziek.tar** krijgt en daarna de het **tar** bestand inpakt in een **gzip** zodat je bijv. een bestand **muziek.tar.gz** krijgt. In het volgende voorbeeld doen we dit met **7-Zip**.

- Installeer [7-zip](https://www.7-zip.org/download.html) als dat programma nog niet beschikbaar is.
- Ga in de gezamenlijke map zoals bijv. **muziek** staan en selecteer alle sub mappen met **Ctrl-A**. Klik op de rechter muis knop en selecteer **7-Zip > Toevoegen aan archief**.
- Selecteer als **Archief formaat: tar** en druk op **OK**.
- Selecteer alleen het aangemaakte **tar** bestand (Soms zie je er geen **.tar** achter staan). Klik op de rechter muis knop en selecteer **7-Zip > Toevoegen aan archief**.
- Selecteer als **Archief formaat: gzip** en druk op **OK**.

Je kunt nu het aangemaakte bestand zoals **muziek.tar.gz** (Soms zie je er geen **.gz** achter staan) als data set gebruiken om een App aan te maken zoals in *Fase3*.

## Herhaal Fase 3

Gebruik de eigen dataset om een App aan te maken volgens de instructies in *Fase 3*. Dit kan iedere leerling weer afzonderlijk doen om eventueel weer een app competitie te houden net als in *Fase 2*