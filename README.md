# Workshop 3DToolboxNL en 3D Leia viewer.

## 3DToolboxNL
Het project 3DToolboxNL is gericht op het beschikbaar maken van open source tooling en documentatie voor het werken met 3D informatie in met name Cesium, in de Nederlandse context.

In deze workshop gebruiken we de 3DToolboxNL om 3D data zoals het GeoTop model (uit de Basisregistratie Ondergrond) en een AHN DEM te converteren naar een open standaard dat zich makkelijk laat inladen in Cesium. https://github.com/3DToolboxNL/3DToolboxNL

## 3D LEIA viewer
We gebruiken de 3D Leia viewer (Cesium) om deze data te visualiseren. Tijdens de workshop gaan de viewer ook installeren. LEIA (https://github.com/leia-project) heeft veel functionaliteit om via een gebruiksvriendelijke interface 2D en 3D data te visualiseren, bevragen, bewerken en analyseren.

Om de installatie van LEIA eenvoudig te houden maken we gebruik van Docker, zorg dus dat dit geïnstalleerd is (https://docs.docker.com/get-docker/). Mocht je geen git client beschikbaar hebben dan kun je de workshop bestanden (deze repository) ook downloaden als zip bestand: https://github.com/ProvincieZeeland/foss4g-nlbe/archive/refs/heads/main.zip. 

De Docker containers zijn gemaakt op basis van de onderstaande url's:

| Container | URL |
| ----------- | ----------- |
| leia-viewer | http://localhost:5000 |
| leia-config | http://localhost:3000 |

Zorg dus dat je de rechten hebt om containers te downloaden / starten en dat poort 3000 en 5000 beschikbaar zijn op je werkstation (mocht je OSX gebruiken dan kan het zijn dat poort 5000 al gebruikt wordt, zie https://developer.apple.com/forums/thread/682332).

### Installatie van de viewer
- Gebruik het git clone commando (of de bovengenoemde zip file) om de bestanden van deze repository te installeren op je lokale werkstation (```git clone git@github.com:ProvincieZeeland/foss4g-nlbe.git .```).
- Mocht clonen via ssh niet werken dan kan het ook via https: ```https://github.com/ProvincieZeeland/foss4g-nlbe.git```
- Maak in de directory waar de bestanden zijn opgeslagen / geplaatst een subdirectory genaamd: ```data/config/acc```
- Kopieer het bestand foss4g.json in /data/config/acc.
- De docker containers kunnen nu worden gestart met ```docker compose up -d```

### Github repo's
https://github.com/ProvincieZeeland/viewer-config-server
https://github.com/leia-project/viewer
