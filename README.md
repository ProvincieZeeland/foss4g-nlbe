# Workshop 3DToolboxNL en 3D Leia viewer.

## 3DToolboxNL
Het project 3DToolboxNL is gericht op het beschikbaar maken van open source tooling en documentatie voor het werken met 3D informatie in met name Cesium, in de Nederlandse context.

In deze workshop gebruiken we de 3DToolboxNL om 3D data zoals het GeoTop model (uit de Basisregistratie Ondergrond) en een AHN DEM te converteren naar een open standaard dat zich makkelijk laat inladen in Cesium. https://github.com/3DToolboxNL/3DToolboxNL

## 3D LEIA viewer
We gebruiken de 3D Leia viewer (Cesium) om deze data te visualiseren. Tijdens de workshop gaan de viewer ook installeren. LEIA (https://github.com/leia-project) heeft veel functionaliteit om via een gebruiksvriendelijke interface 2D en 3D data te visualiseren, bevragen, bewerken en analyseren.

Om de installatie van LEIA eenvoudig te houden maken we gebruik van Docker, zorg dus dat dit geïnstalleerd is (https://docs.docker.com/get-docker/). Docker Desktop is prima. Een account op GitHub is ook aan te raden. Mocht je geen git client beschikbaar hebben dan kun je de workshop bestanden (deze repository) ook downloaden als zip bestand: https://github.com/ProvincieZeeland/foss4g-nlbe/archive/refs/heads/main.zip. 

De Docker containers zijn gemaakt op basis van de onderstaande url's:

| Container | URL |
| ----------- | ----------- |
| leia-viewer | http://localhost:5000 |
| leia-config | http://localhost:3000 |

Zorg dus dat je de rechten hebt om containers te downloaden / starten en dat poort 3000 en 5000 beschikbaar zijn op je werkstation (mocht je OSX gebruiken dan kan het zijn dat poort 5000 al gebruikt wordt, zie https://developer.apple.com/forums/thread/682332).

### Installatie van de viewer
- Start je Windows command prompt met het cmd commando (of start een Linux terminal venster) en maak een werkdirectory aan waarin je alle rechten hebt.
- Gebruik het git clone commando (of de bovengenoemde zip file) om de bestanden van deze repository te installeren op je lokale werkstation: ```git clone git@github.com:ProvincieZeeland/foss4g-nlbe.git .```
- Mocht clonen via ssh niet werken dan kan het ook via https: ```git clone https://github.com/ProvincieZeeland/foss4g-nlbe.git .```

![image](https://github.com/user-attachments/assets/c473abfb-6d0c-4459-80b5-00aff5d710d0)

- Maak in de directory waar de bestanden zijn opgeslagen / geplaatst een subdirectory genaamd: ```data/config/acc``` (of Windows: data\config\acc).
- Kopieer het bestand foss4g.json (uit de Leia github repository) naar de net aangemaakt directory data/config/acc (of Windows: data\config\acc).
  ![image](https://github.com/user-attachments/assets/25cf1a17-bc40-457e-a2de-c661d9dd30d1)

- De docker containers kunnen nu worden gestart met ```docker compose up -d```.
- Gebruik je Docker Editor dan zie je de containers verschijnen in de Docker Editor.
  ![image](https://github.com/user-attachments/assets/90477302-3216-4d5a-b68e-71de40b2a07b)

- Mocht de compose de containers niet kunnen downloaden geef dan de volgende commanda's in je DOS box: ```docker pull wkosten/leia-viewer-foss4g-nlbe``` en ```docker pull wkosten/leia-config-foss4g-nlbe``` waarna de compose alsnog gestart kan worden dmv ```docker compose up -d```.

![image](https://github.com/user-attachments/assets/240d8aee-3ef9-485f-b394-c40f02805abe)
 
- Om de containers te stoppen kun je ```docker compose down``` in typen.


### Zelf wijzigingen maken
- Open in je favoriete code editor het bestandje data\config\acc\foss4g.json Dit is het centrale bestand waarmee je data in de viewer kan bijladen, bookmarks kan aanmaken en alle verdere configuratie van de Leia viewer kan instellen.

- Sla de wijzigen op en bekijk in je browser de Leia viewer: ```http://localhost:5000/foss4g```
- Na iedere wijzigen moet de browser opnieuw geladen worden (bv ctrl-F5).



   
### Github repo's
https://github.com/ProvincieZeeland/viewer-config-server
https://github.com/leia-project/viewer
