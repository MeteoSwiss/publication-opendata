*Version, status:* v1.1, Draft / [change log](https://github.com/MeteoSwiss/publication-opendata/commits/main) <br>
*Maintainer:* Federal Office of Meteorology and Climatology MeteoSwiss, [OGD@MeteoSwiss project team](mailto:opendata@meteoswiss.ch)

<!-- [![GitHub commit](https://img.shields.io/github/last-commit/MeteoSwiss/publication-opendata)](https://github.com/MeteoSwiss/publication-opendata/commits/master) -->

[En français](#contexte-et-principaux-défis) | [In italiano](#contesto-e-sfide-principali) | [In English](#background-and-key-challenges)

# Willkommen bei der Bereitstellung von 'Open Government Data (OGD)' von MeteoSchweiz

## Hintergrund und zentrale Herausforderungen

Mit der Einführung der [Totalrevision der Verordnung über die Meteorologie und Klimatologie (MetV)](https://www.fedlex.admin.ch/de/consultation-procedures/ended/2023#https://fedlex.data.admin.ch/eli/dl/proj/2022/77/cons_1) - voraussichtlich per 1. Januar 2025 - wird Meteoschweiz die im gesetzlichen Auftrag erhobenen Daten von den Gebühren befreien und damit den Zugang zu offenen Daten umsetzen, wie es das [Bundesgesetz über den Einsatz elektronischer Mittel zur Erfüllung von Behördenaufgaben (EMBAG)](https://www.fedlex.admin.ch/eli/cc/2023/682/de) fordert. Die von MeteoSchweiz angestrebte Kompatibilität mit der ['High Value Datasets (HVD)'-Richtlinie der EU (s. Anhang, Kapitel 3. "Meteorologie")](https://eur-lex.europa.eu/legal-content/DE/TXT/HTML/?uri=CELEX:32023R0138#d1e32-48-1) und die Forderungen des EMBAG führen zu einen Umstieg des Datenzugangs von 'Push' (d.h. auf Anfrage/Bestellung) zu 'Pull' (d.h. per Selbstbedienung).

MeteoSchweiz stellt seit Jahrzehnten meteorologische und klimatologische Daten auf internationaler, europäischer und nationaler Ebene bereit. Seit 2012 hat MeteoSchweiz zudem [Erfahrungen mit der Bereitstellung offener Daten aufgebaut (s. Datensätze beginnend mit "ch.meteoschweiz...")](https://data.geo.admin.ch/). Dazu nutzt MeteoSchweiz die [Bundes-Geodaten-Infrastruktur BGDI](https://www.geo.admin.ch/de/allgemeine-nutzungsbedingungen-bgdi), die von [swisstopo](https://www.swisstopo.admin.ch/de) betrieben wird.

Der Zugang zu offenen Daten soll überarbeitet und vereinfacht werden, so dass Menschen mit unterschiedlichen datentechnischen und meteorologischen Kenntnissen die gewünschten Daten ohne Mühe finden können. Anwendungsorientierte Beschreibungen und Kontextinformationen helfen ihnen einzuschätzen, ob bzw. unter welchen Bedingungen welche Daten für eine gewünschte Anwendung passen.

## Vision, Mission und Strategie für Version 1.0

### Unsere Vision ist, dass jedeR die richtigen offenen meteorologischen und klimatologischen Daten von MeteoSchweiz leicht finden und nutzen kann. Wir garantieren maximale Kompatibilität mit den offenen Daten der europäischen und internationalen Partnerbehörden.

**Unsere Mission** ist, 
die Bereitstellung aller offenen Daten so zu gestalten, dass sie dieselbe Zuverlässigkeit und Sorgfalt widerspiegeln, die MeteoSchweiz den Menschen und Organisationen entgegenbringt, denen sie heute bereits dient.

**Unsere Strategie** für die Version 1.0 ist, 
allen Nutzerinnen und Nutzern zu ermöglichen, offene Daten als Files via die STAC-API der BGDI herunterzuladen.

Damit entspricht die OGD-Bereitstellung von MeteoSchweiz in der Version 1.0 der Anforderung der HVD-Richtlinie der EU, "Datensätze (...) über Massen-Download (...) zur Weiterverwendung zur Verfügung zu stellen" ([Anhang, Kapitel 3.2. a](https://eur-lex.europa.eu/legal-content/DE/TXT/HTML/?uri=CELEX:32023R0138#d1e32-48-1)). Die Anforderung, Datensätze auch über APIs verfügbar zu machen, setzt MeteoSchweiz darauf in einer späteren Umsetzungsetappe um.

**Unsere wichtigsten Ergebnisse** für die Version 1.0 sind:
1. Aus den Quellsystemen der verschiedenen Datentypen (Bodenstationsdaten und Beobachtungen, Klimadaten und räumliche Klimaanalysen, Radardaten, Prognosedaten, Atmosphärendaten) werden die zusammen mit den entsprechenden Fachspezialistinnen und -spezialisten [spezifizierten OGD-Produkte](#21-overview-of-data-types-to-be-made-available-as-open-data) und ihre 'File Metadata' laufend als Files generiert.
2. Alle Files werden laufend auf die definierten 'Collections' in der STAC-API der BGDI übertragen und als 'Assets' zu den entsprechenden 'Items' abgelegt.
3. Zu jeder 'Collection' ist ein entsprechender 'Discovery Metadata'-Datensatz im Geometadatenkatalog [geocat.ch](https://www.geocat.ch/geonetwork/srv/ger/catalog.search#/home) angelegt. Geocat.ch integriert die 'Discovery Metadata' in den OGD-Metadatenkatalog der Schweizer Behörden [opendata.swiss](https://opendata.swiss/de), und opendata.swiss in den europäischen OGD-Metadatenkatalog [data.europa.eu](https://data.europa.eu/de).
4. Die Nutzerinnen und Nutzer können einzelne und mehrere Files über ein WebGUI bei MeteoSchweiz manuell herunterladen oder über die STAC-API der BGDI automatisiert beziehen.

**Unsere wichtigsten Nutzendengruppen** für die Version 1.0 sind:
1. Menschen mit wenig Meteo- und unterschiedlichen datentechnischen Kenntnissen,
2. Menschen mit mittleren Meteo- und unterschiedlichen datentechnischen Kenntnissen,
3. Menschen mit hohen Meteo- und hohen datentechnischen Kenntnissen.

> [!NOTE]
> Unsere Nutzendenschaft ist sehr breit und unterschiedlich. Zur Priorisierung der Funktionalitäten sowie der anwendungsorientierten Beschreibungen und Kontextinformationen der Daten haben wir diese grobe Gruppierung gewählt. Die Gruppen sind von oben nach unten nach ihrer Anzahl (viele > wenige) aufgelistet.

## Strategie und Releaseplanung

**Strategie für die Priorisierung**
1. Beta-Version - Einzelne Komponenten als Prototyp entwickeln, um wichtige Entscheidungen zu treffen und Risiken zu bewerten
2. Version 1.0 - **Für die Lancierung unbedingt notwendige** Funktionalitäten realisieren und OGD-Produkte bereitstellen
3. Als nächstes - Weitere definierte OGD-Produkte bereitstellen
4. Später - Weitere Funktionalitäten (u.a. Daten abfragen via API-Features) realisieren

**Roadmap der OGD-Bereitstellung** <br>
Aufgeführt sind Hauptfunktionalitäten für Nutzerinnen und Nutzer sowie die OGD-Datenprodukte (mit OGD-Produktnummern).

| Beta-Version | Version 1.0 | Als nächstes | Später |
| :----------- | :---------- | :----------- | :----- |
| Einzelne oder mehrere Files über ein WebGUI manuell herunterladen |              |              | Ausgewählte Daten über ein API-Features abfragen |
| Einzelne oder mehrere Files über die STAC-API der BGDI automatisiert beziehen |              |              |        |
|              | **Messwerte:** <br> [Automatische Wetterstationen, Niederschlagsstationen, Grenzschichtstationen](#231-automatic-weather-stations-smn-smn-precip-smn-tower) (01, 02, 03) <br> [Manuelle und Totalisator-Niederschlagsstationen](#232-manual-precipitation-stations-nime-tot) (04, 05) <br> [Pollenstationen](#235-swiss-pollen-monitoring-stations-pollen) (10) <br> [Radiosondierungen](#241-radio-soundings-radiosounding) (12) |              |        | 
|              | **Beobachtungen:** <br> [Meteorologische Augenbeobachtungen](#233-visual-observations-obs) (06) <br> [Phänologische Beobachtungen](#236-phenological-observations-phenology) (11) |              |        | 
|              | **Homogene Messwerte:** <br> [Klimastationen und Niederschlags-Klimastationen](#234-climate-stations-swiss-nbcn-nbcn-nbcn-precip) (07, 08) |              |        | 
|              | **Gitterdaten:** <br> [Boden- und satellitengestützte räumliche Klimadaten](#261-spatial-climate-data) (16, 17) |              |        |
|              | **Gitterdaten:** <br> [Grundlegende und erweiterte Radardaten](#262-radar-and-combiprecip-data) (18, 19) <br> [Kombinierte Niederschlagsberechnungen](#2623-combiprecip-data) (20) |              |        | 
|              | **Gitterdaten:** <br> [Kurzfristprognosedaten](#251-inca-data-nowcasting) (13) <br> [Prognosedaten](#252-cosmoicon-data-forecasting) (14) |              |        | 
|              | **Punktdaten:** <br> [Lokalprognosedaten](#253-postprocessed-local-forecast-data-data4web) (15) |              |        | 

> [!NOTE]
> Die Planung wird laufend aktualisiert und kann sich entsprechend ändern. Ab Juli 2024 wird sie für die [Datenprodukte](#21-overview-of-data-types-to-be-made-available-as-open-data) etappiert vorliegen und hier entsprechend kommuniziert.

## Kontakt zum Projekt

Für alle Fragen zum Projekt, wenden Sie sich bitte an: [opendata(at)meteoswiss.ch](mailto:opendata@meteoswiss.ch)

<!-- Bleiben Sie auf dem Laufenden und [abonnieren](..) Sie unseren OGD-Newsletter, indem sie auf den Link klicken. Oder senden Sie ein E-Mail an [ogd-news(at)news.meteoswiss.ch](mailto:ogd-news@news.meteoswiss.ch) mit dem Betreff 'JOIN ogd_list'. -->

---

# Bienvenue à la mise à disposition 'Open Government Data (OGD)' de MétéoSuisse

## Contexte et principaux défis

Avec l'introduction de la [Révision totale de l’ordonnance sur la météorologie et la climatologie (OMét)](https://www.fedlex.admin.ch/fr/consultation-procedures/ended/2023#https://fedlex.data.admin.ch/eli/dl/proj/2022/77/cons_1) - probablement au 1er janvier 2025 - MétéoSuisse exonérera des émoluments les données collectées sur mandat légal et mettra ainsi en œuvre l'accès aux données ouvertes, comme l'exige la [Loi fédérale sur l’utilisation de moyens électroniques pour l’exécution des tâches des autorités (LMETA)](https://www.fedlex.admin.ch/eli/cc/2023/682/fr). La compatibilité souhaitée par MétéoSuisse avec la Directive de l'UE ['High Value Datasets (HVD)' (voir annexe, chapitre 3. «Météorologique»)](https://eur-lex.europa.eu/legal-content/FR/TXT/HTML/?uri=CELEX:32023R0138#d1e32-48-1) et les exigences de la LMETA entraînent un passage de l'accès aux données de 'Push' (c'est-à-dire sur demande/commande) à 'Pull' (c'est-à-dire en libre-service).

Depuis des décennies, MétéoSuisse met à disposition des données météorologiques et climatologiques au niveau international, européen et national. Depuis 2012, MétéoSuisse a en outre [acquis de l'expérience dans la mise à disposition de données ouvertes (cf. jeux de données commençant par «ch.meteoschweiz...»)](https://data.geo.admin.ch/). Pour ce faire, MétéoSuisse utilise l’[Infrastructure fédérale de données géographiques IFDG](https://www.geo.admin.ch/fr/conditions-generales-utilisation-ifdg), gérée par [swisstopo](https://www.swisstopo.admin.ch/fr).

L'accès aux données ouvertes doit être revu et simplifié afin que les personnes ayant des connaissances différentes en matière de technique de données et de météorologie puissent trouver sans peine les données souhaitées. Des descriptions orientées vers les applications et des informations contextuelles les aident à évaluer si, et dans quelles conditions, quelles données conviennent à une application souhaitée.

## Vision, mission et stratégie pour la version 1.0

### Notre vision est que chacun puisse trouver et utiliser facilement les données météorologiques et climatologiques ouvertes appropriées de MétéoSuisse. Nous garantissons une compatibilité maximale avec les données ouvertes des autorités partenaires européennes et internationales.

**Notre mission** est, 
de faire en sorte que la mise à disposition de toutes les données ouvertes reflète la même fiabilité et le même soin que MétéoSuisse apporte aux personnes et aux organisations qu'il sert déjà aujourd'hui.

**Notre stratégie** pour la version 1.0 est, 
de permettre à tous les utilisateurs de télécharger des données ouvertes sous forme de fichiers via l'API STAC de l'IFDG.

La mise à disposition OGD de MétéoSuisse dans la version 1.0 répond ainsi à l'exigence de la directive HVD de l'UE de mettre à disposition des «ensembles de données en vue de leur réutilisation (...) sous la forme d’un téléchargement en masse» ([Annexe, chapitre 3.2. a](https://eur-lex.europa.eu/legal-content/DE/TXT/HTML/?uri=CELEX:32023R0138#d1e32-48-1)). L'exigence de rendre les jeux de données également disponibles par l’intermédiaire d’API sera mise en œuvre par MétéoSuisse au cours d'une étape ultérieure.

**Nos principaux résultats** pour la version 1.0 sont les suivants :
1. A partir des systèmes sources des différents types de données (données de stations au sol et observations, données climatiques et analyses spatiales du climat, données radar, données en prévision, données atmosphériques), les [produits OGD spécifiés avec les spécialistes correspondants](#21-overview-of-data-types-to-be-made-available-as-open-data) et leurs 'File Metadata' sont générés en permanence sous forme de fichiers.
2. Tous les fichiers sont transférés en permanence sur les 'collections' définies dans l'API STAC de l'IFDG et enregistrés comme 'assets' pour les 'items' correspondants.
3. Un jeu de données 'Discovery Metadata' correspondant est créé pour chaque 'collection' dans le Catalogue de géométadonnées [geocat.ch](https://www.geocat.ch/geonetwork/srv/fre/catalog.search#/home). Geocat.ch intègre les 'Discovery Metadata' dans le Catalogue de métadonnées OGD de l’administration publique suisse [opendata.swiss](https://opendata.swiss/fr), et opendata.swiss dans le Catalogue de métadonnées OGD européen [data.europa.eu](https://data.europa.eu/fr).
4. Les utilisateurs peuvent télécharger manuellement un ou plusieurs fichiers via une WebGUI auprès de MétéoSuisse ou les obtenir de manière automatisée via l'API STAC de l'IFDG.

**Nos principaux groupes d'utilisateurs** pour la version 1.0 sont :
1. les personnes ayant peu de connaissances météorologiques et différentes connaissances techniques en matière de données,
2. les personnes ayant des connaissances moyennes en météorologie et en différentes techniques de données,
3. les personnes ayant des connaissances élevées en météorologie et en technique des données.

> [!NOTE]
> Notre groupe d'utilisateurs est très large et varié. Nous avons choisi ce regroupement approximatif pour prioriser les fonctionnalités ainsi que les descriptions orientées vers l'application et les informations contextuelles des données. Les groupes sont listés de haut en bas en fonction de leur nombre (nombreux > peu).

## Stratégie et planification des versions

**Stratégie de priorisation**.
1. Version Beta - Développer des composants individuels en tant que prototype afin de prendre des décisions importantes et d'évaluer les risques.
2. Version 1.0 - **Réaliser les fonctionnalités absolument nécessaires** pour le lancement et mettre à disposition des produits OGD.
3. Ensuite - Mettre à disposition d'autres produits OGD définis.
4. Plus tard - Réaliser d'autres fonctionnalités (notamment consulter les données par un 'API features').

**La feuille de route de la mise à disposition OGD** <br>.
Les fonctionnalités principales pour les utilisateurs ainsi que les produits de données OGD (avec les numéros de produits OGD) sont indiqués.

| Version Beta | Version 1.0 | Ensuite | Plus tard |
| :----------- | :---------- | :----------- | :----- |
| Télécharger manuellement un ou plusieurs fichiers via 'WebGUI' | | | Consulter des données sélectionnées par un 'API Features' |
| Obtenir un ou plusieurs fichiers de manière automatisée via l'API STAC de l'IFDG | | |
| | **Valeurs mesurées:** <br> [Stations automatiques météorologiques, pluviométriques et de la couche limite](#231-automatic-weather-stations-smn-smn-precip-smn-tower) (01, 02, 03) <br> [Stations manuelles pluviométriques et totalisateur](#232-manual-precipitation-stations-nime-tot) (04, 05) <br> [Stations pollen](#235-swiss-pollen-monitoring-stations-pollen) (10) <br> [Radiosondages](#241-radio-soundings-radiosounding) (12) | | 
| | **Observations:** <br> [Observations visuelles météorologiques](#233-visual-observations-obs) (06) <br> [Observations phénologiques](#236-phenological-observations-phenology) (11) | | 
| | **Valeurs mesurées homogénéisées:** <br> [Stations climatiques et stations climatiques de précipitations](#234-climate-stations-swiss-nbcn-nbcn-nbcn-precip) (07, 08) | | 
| | **Données matricielles:** <br> [Données climatiques spatiales basées sur le sol et les satellites](#261-spatial-climate-data) (16, 17) | |
| | **Données matricielles:** <br> [Données radar de base et avancées](#262-radar-and-combiprecip-data) (18, 19) <br> [Calculs combinés des précipitations](#2623-combiprecip-data) (20) | | 
| | **Données matricielles:** <br> [Données de prévisions à court terme](#251-inca-data-nowcasting) (13) <br> [Données de prévisions](#252-cosmoicon-data-forecasting) (14) | | 
| | **Données ponctuelles:** <br> [Données de prévisions locales](#253-postprocessed-local-forecast-data-data4web) (15) | | 

> [!NOTE]
> La planification est actualisée en permanence et peut être modifiée en conséquence. A partir de juillet 2024, elle sera disponible par étapes pour les [produits de données](#21-overview-of-data-types-to-be-made-available-as-open-data) et sera communiquée ici en conséquence.

## Contact avec le projet

Pour toute question concernant le projet, veuillez vous adresser à : [opendata(at)meteoswiss.ch](mailto:opendata@meteoswiss.ch)

<!-- Tenez-vous au courant et [abonnez-vous](..) à notre newsletter OGD en cliquant sur le lien. Ou envoyez un e-mail à [ogd-news(at)news.meteoswiss.ch](mailto:ogd-news@news.meteoswiss.ch) avec le sujet 'JOIN ogd_list'. -->

---

# Benvenuti nell'offerta “Open Government Data (OGD)” di MeteoSvizzera

## Contesto e sfide principali

Con l'introduzione della [Revisione totale dell’ordinanza sulla meteorologia e la climatologia (OMet)](https://fedlex.data.admin.ch/eli/dl/proj/2022/77/cons_1) - probabilmente per il 1° gennaio 2025 - MeteoSvizzera esenterà dalle tasse i dati raccolti nell'ambito del mandato legale, implementando così l'accesso ai dati aperti, come richiesto dalla [Legge federale
concernente l’impiego di mezzi elettronici per l’adempimento dei compiti delle autorità
(LMeCA)](https://www.fedlex.admin.ch/eli/cc/2023/682/it). La compatibilità con la Direttiva UE [“High Value Datasets (HVD)” (vedi Allegato, Capitolo 3. “Dati meteorologici”)](https://eur-lex.europa.eu/legal-content/IT/TXT/HTML/?uri=CELEX:32023R0138#d1e32-48-1), a cui MeteoSvizzera sta puntando, e i requisiti della LMeCA stanno portando a un cambiamento nell'accesso ai dati da “push” (cioè su richiesta/ordine) a “pull” (cioè tramite self-service).

MeteoSvizzera fornisce da decenni dati meteorologici e climatologici a livello internazionale, europeo e nazionale. Dal 2012, MeteoSvizzera ha anche [accumulato esperienza nella fornitura di dati aperti (vedi i dataset che iniziano con “ch.meteoschweiz...”)](https://data.geo.admin.ch/). A questo scopo, MeteoSvizzera utilizza l'[Infrastruttura federale di dati geografici IFDG](https://www.geo.admin.ch/it/condizioni-generali-di-utilizzo-ifdg), gestita da [swisstopo](https://www.swisstopo.admin.ch/it).

L'accesso ai dati aperti deve essere rivisto e semplificato in modo che persone con diversi livelli di tecnologia dei dati e di conoscenze meteorologiche possano trovare facilmente i dati desiderati. Le descrizioni orientate all'applicazione e le informazioni contestuali aiutano a valutare se e in quali condizioni i dati sono adatti all'applicazione desiderata.

## Visione, missione e strategia per la versione 1.0

### La nostra visione è che tutti possano facilmente trovare e utilizzare i giusti dati meteorologici e climatologici aperti di MeteoSvizzera. Garantiamo la massima compatibilità con i dati aperti delle autorità partner europee e internazionali.

**La nostra missione** è, 
rendere disponibili tutti i dati aperti in modo che riflettano la stessa affidabilità e cura che MeteoSvizzera fornisce alle persone e alle organizzazioni che già oggi serve.

**La nostra strategia** per la versione 1.0 è, 
consentire a tutti gli utenti di scaricare i dati aperti come file attraverso l'API STAC del IFDG.

La fornitura di OGD di MeteoSvizzera nella versione 1.0 soddisfa quindi il requisito della Direttiva HVD dell'UE di mettere a disposizione “le serie di dati (...) per il riutilizzo tramite download in blocco” ([Allegato, capitolo 3.2. a](https://eur-lex.europa.eu/legal-content/IT/TXT/HTML/?uri=CELEX:32023R0138#d1e32-48-1)). MeteoSvizzera implementerà il requisito di rendere disponibili i set di dati anche tramite API Features in una fase di implementazione successiva.

**I nostri risultati più importanti** per la versione 1.0 sono:
1. Dai sistemi di origine dei vari tipi di dati (dati delle stazioni al suolo e osservazioni, dati climatici e analisi spaziali del clima, dati radar, dati di previsione, dati atmosferici), i prodotti OGD [specificati insieme ai relativi specialisti] (#21-overview-of-data-types-to-be-to-be-made-available-as-open-data) e i loro “File Metadata” sono continuamente generati come file.
2. Tutti i file vengono continuamente trasferiti nelle “Collections” definite nell'API STAC del IFDG e memorizzati come “Assets” per i corrispondenti “Items”.
3. Per ogni “Collection” viene creato un corrispondente set di dati “Discovery Metadata” nel Catalogo dei Geometadati [geocat.ch](https://www.geocat.ch/geonetwork/srv/ita/catalog.search#/home). Geocat.ch integra i “Discovery Metadata” nel Catalogo dei metadati OGD delle autorità svizzere [opendata.swiss](https://opendata.swiss/it), e opendata.swiss nel Catalogo europeo dei metadati OGD [data.europa.eu](https://data.europa.eu/it).
4. Gli utenti possono scaricare file singoli o multipli manualmente tramite una WebGUI di MeteoSvizzera o ottenerli automaticamente tramite l'API STAC del IFDG.

**I nostri gruppi di utenti** più importanti per la versione 1.0 sono:
1. persone con scarse conoscenze meteorologiche e diversi livelli di conoscenza dei dati tecnici,
2. persone con un livello medio di conoscenza meteorologica e vari livelli di conoscenza dei dati tecnici,
3. persone con un livello elevato di conoscenze meteorologiche e di dati.

> [!NOTA]
> La nostra base di utenti è molto ampia e diversificata. Abbiamo scelto questo raggruppamento di massima per considerare prioritarie le funzionalità, le descrizioni orientate all'applicazione e le informazioni sul contesto dei dati. I gruppi sono elencati dall'alto verso il basso in base al loro numero (molti > pochi).

## Strategia e pianificazione del rilascio

**Strategia per la definizione delle priorità**
1. Versione Beta - Sviluppare i singoli componenti come prototipi per prendere decisioni importanti e valutare i rischi
2. Versione 1.0 - **Realizzare le funzionalità assolutamente necessarie** per il lancio e fornire prodotti OGD
3. Successiva - Fornire prodotti OGD ulteriormente definiti
4. Più tardi - Realizzare ulteriori funzionalità (compreso il reperimento dei dati tramite 'API Features')

**Roadmap dell'offerta OGD** <br>
Sono elencate le principali funzionalità per gli utenti e i prodotti OGD (con i numeri dei prodotti OGD).

| Versione Beta | Versione 1.0 | Successiva | Più tardi |
| :------------ | :----------- | :--------- | :-------- |
| Scaricare manualmente file singoli o multipli tramite una WebGUI |  |  | Interrogare i dati selezionati tramite una funzione API |
| Ottenere automaticamente file singoli o multipli tramite l'API STAC del BGDI |  |  |  |
| | **Valori misurati:** <br> [Stazioni meteorologiche automatiche, pluviometriche automatiche e dello strato limite automatiche](#231-automatic-weather-stations-smn-smn-precip-smn-tower) (01, 02, 03) <br> [Stazioni pluviometriche manuali e di precipitazione totalizzatori](#232-stazioni-manuali-di-precipitazione-nime-tot) (04, 05) <br> [Stazioni pollini](#235-stazioni-svizzere-di-monitoraggio-polline) (10) <br> [Radiosondaggi](#241-radio-sondaggi-radiosondaggi) (12) | | | 
| | **Osservazioni:** <br> [Osservazione visuale meteorologiche](#233-osservazioni-visive-obs) (06) <br> [Osservazioni fenologiche](#236-osservazioni-fenologia) (11) | | | 
| | **Valori misurati omogeneizzati:** <br> [Stazioni climatologiche e climatologiche pluviometriche](#234-stazioni-climatiche-swiss-nbcn-nbcn-nbcn-precip) (07, 08) | | |
| | **Dati a matrice:** <br> [Dati climatici spaziali da terra e da satellite](#261-spatial-climate-data) (16, 17) | | |
| | **Dati a matrice:** <br> [Dati radar di base ed avanzati](#262-radar-e-combiprecip-data) (18, 19) <br> [Calcoli di precipitazione combinati](#2623-combiprecip-data) (20) | | |
| | **Dati a matrice:** <br> [Dati di previsione a breve termine](#251-inca-data-nowcasting) (13) <br> [Dati di previsione](#252-cosmoicon-data-forecasting) (14) | | |
| | **Dati puntuali:** <br> [Dati delle previsioni locali](#253-postprocessed-local-forecast-data-data4web) (15) | | | 

> [!NOTA]
> La pianificazione è in continuo aggiornamento e può subire variazioni. A partire da luglio 2024, sarà disponibile per gradi per i [prodotti di dati](#21-overview-of-data-types-to-be-to-be-available-as-open-data) e comunicato qui di conseguenza.

## Contatti per il progetto

Per tutte le domande sul progetto, si prega di contattare: [opendata(at)meteoswiss.ch](mailto:opendata@meteoswiss.ch)

<!-- Rimanete aggiornati e [iscrivetevi](..) alla nostra newsletter OGD cliccando sul link. Oppure inviate un'e-mail a [ogd-news(at)news.meteoswiss.ch](mailto:ogd-news@news.meteoswiss.ch) con oggetto 'JOIN ogd_list'. -->

---

# Welcome to the 'Open Government Data (OGD)' provision of MeteoSwiss

## Background and key challenges

With the introduction of the [Totalrevision der Verordnung über die Meteorologie und Klimatologie (MetV)](https://www.fedlex.admin.ch/de/consultation-procedures/ended/2023#https://fedlex.data.admin.ch/eli/dl/proj/2022/77/cons_1) - expected on 1 January 2025 - MeteoSwiss will exempt the data collected under the legal mandate from fees and thus implement access to open data, as required by the [Bundesgesetz über den Einsatz elektronischer Mittel zur Erfüllung von Behördenaufgaben (EMBAG)](https://www.fedlex.admin.ch/eli/cc/2023/682/de). The compatibility with the EU's ['High Value Datasets (HVD)' Directive (see Annex, Chapter 3. ‘Meteorological’)](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:32023R0138#d1e32-48-1) that MeteoSwiss is striving for and the requirements of EMBAG are leading to a change in data access from 'push' (i.e. on request/order) to 'pull' (i.e. via self-service).

MeteoSwiss has been providing meteorological and climatological data at international, European and national level for decades. Since 2012, MeteoSwiss has also [built up experience with the provision of open data (see datasets beginning with ‘ch.meteoschweiz...’)](https://data.geo.admin.ch/). To this end, MeteoSwiss uses the [Federal Spatial Data Infrastructure FSDI](https://www.geo.admin.ch/en/general-terms-of-use-fsdi), which is operated by [swisstopo](https://www.swisstopo.admin.ch/en).

Access to open data must be revised and simplified so that people with different levels of data technology and meteorological knowledge can easily find the required data. Application-orientated descriptions and contextual information help them to assess whether and under what conditions which data is suitable for a particular application.

## Vision, mission and strategy for version 1.0

### Our vision is that everyone can easily find and use the right open meteorological and climatological data from MeteoSwiss. We guarantee maximum compatibility with the open data of European and international partner agencies.

**Our mission** is, 
to make all open data available in such a way that it reflects the same reliability and care that MeteoSwiss provides to the people and organisations it already serves today.

**Our strategy** for version 1.0 is, 
to enable all users to download open data as files via the STAC API of the FSDI.

The OGD provision of MeteoSwiss in version 1.0 thus fulfils the requirement of the EU's HVD Directive to make ‘datasets (...) available for re-use (...) through bulk download’ ([Annex, Chapter 3.2. a](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:32023R0138#d1e32-48-1)). The requirement to make datasets also available via APIs will be implemented by MeteoSwiss in a later implementation stage.

**Our primary outcomes** for version 1.0 include:
1. From the source systems of the various data types (ground station data and observations, climate data and spatial climate analyses, radar data, forecast data, atmospheric data), the OGD products [specified together with the corresponding specialists](#21-overview-of-data-types-to-be-made-available-as-open-data) and their 'file metadata' are continuously generated as files.
2. All files are continuously transferred to the defined 'collections' in the STAC API of the FSDI and stored as 'assets' for the corresponding 'items'.
3. For each collection, a corresponding 'discovery metadata' dataset is created in the geometadata catalogue [geocat.ch](https://www.geocat.ch/geonetwork/srv/eng/catalog.search#/home). Geocat.ch integrates the 'discovery metadata' into the OGD metadata catalogue of the Swiss authorities [opendata.swiss](https://opendata.swiss/en), and opendata.swiss into the European OGD metadata catalogue [data.europa.eu](https://data.europa.eu/en).
4. Users can download one or more files manually from MeteoSwiss via a WebGUI or obtain them automatically via the STAC API of the FSDI.

**Our primary users** for version 1.0 include:
1. People with little meteorological knowledge and varying levels of technical data knowledge,
2. People with medium meteorological knowledge and varying levels of technical data knowledge,
3. People with high meteorological and technical data knowledge.

> [!NOTE]
> Our user base is very broad and diverse. We have chosen this rough grouping to prioritise the functionalities as well as the application-oriented descriptions and context information of the data. The groups are listed from top to bottom according to their number (many > few).

## Strategy and release planning

**Strategy for prioritisation**
1. Beta version - Develop individual components as prototypes to make important decisions and assess risks
2. Version 1.0 - Realise functionalities and provide OGD products **absolutely necessary for the launch**
3. Next - Provide further defined OGD products
4. Later - Realise further functionalities (including querying data via API features)

**Roadmap of the OGD provision** <br>
Listed are the main functionalities for users and the OGD data products (with OGD product numbers).

| Beta version | Version 1.0 | Next | Later |
| :----------- | :---------- | :----------- | :----- |
| Manually download single or multiple files via a WebGUI | | Query selected data via an API features | |
| Obtain single or multiple files automatically via the STAC API of the FSDI | | | |
| | **Measured values: ** <br> [Automatic weather stations, precipitation stations, boundary layer stations](#231-automatic-weather-stations-smn-smn-precip-smn-tower) (01, 02, 03) <br> [Manual and totaliser precipitation stations](#232-manual-precipitation-stations-nime-tot) (04, 05) <br> [Pollen stations](#235-swiss-pollen-monitoring-stations-pollen) (10) <br> [Radiosoundings](#241-radio-soundings-radiosounding) (12) | | | 
| | **Observations:** <br> [Meteorological visual observations](#233-visual-observations-obs) (06) <br> [Phenological observations](#236-phenological-observations-phenology) (11) | | |
| | **Homogeneous measured values:** <br> [Climate stations and precipitation-climate stations](#234-climate-stations-swiss-nbcn-nbcn-nbcn-nbcn-precip) (07, 08) | | | 
| | **Grid data:** <br> [Ground and satellite-based spatial climate data](#261-spatial-climate-data) (16, 17) | | | |
| | **Grid data:** <br> [Basic and extended radar data](#262-radar-and-combiprecip-data) (18, 19) <br> [Combined precipitation calculations](#2623-combiprecip-data) (20) | | |
| | **Grid data:** <br> [Short-term forecast data](#251-inca-data-nowcasting) (13) <br> [Forecast data](#252-cosmoicon-data-forecasting) (14) | | | 
| | **Point data:** <br> [Local forecast data](#253-postprocessed-local-forecast-data-data4web) (15) | | | 

> [!NOTE]
> The planning is continuously updated and may change accordingly. From July 2024, it will be available on a staged basis for the [data products](#21-overview-of-data-types-to-be-made-available-as-open-data) and communicated here accordingly.

## Contact for the project

For all questions about the project, please contact: [opendata(at)meteoswiss.ch](mailto:opendata@meteoswiss.ch)

<!-- Stay up to date and [subscribe](..) to our OGD newsletter by clicking on the link. Or send an e-mail to [ogd-news(at)news.meteoswiss.ch](mailto:ogd-news@news.meteoswiss.ch) with the subject 'JOIN ogd_list'. -->

---

Ab hier nur auf Englisch | A partir d'ici, uniquement en anglais | Da qui in poi solo in inglese

# Specification of OGD data products and sample data

## 1. Context and mission of the project
Jump to the [introduction in English above]().

<!-- **Finding out, collecting, analysing and weighting user needs** is the central way for the project team to be able to offer good 'Open Data products'. Thank you very much for your attention and your openness to enter into an exchange with us on this matter. -->

### 1.1. Purpose of this repository
This repository is used by MeteoSwiss' project team to inform potential users interested in Open Data about the plans and to receive specific feedback from them on proposals.
1. [We describe the various 'Open Data products'](https://github.com/MeteoSwiss/publication-opendata/tree/main#2-open-data-products) being designed by MeteoSwiss' specialist data teams. That is: the **data structures, formats, denominations, update frequencies, volumes and other specifics**.
2. We are looking for your feedback on our proposals. To this end, **[we ask you specific questions](https://github.com/MeteoSwiss/publication-opendata/tree/main#12-questions-to-the-open-data-user-community)**.
3. Furthermore we are open to your questions. **Please [share them with us and the community by creating a public issue](https://github.com/MeteoSwiss/publication-opendata/issues/new)**, or [write us an email](https://github.com/MeteoSwiss/publication-opendata/tree/main#13-general-contact-point). You can find all issues - open and closed - sorted by update date [here](https://github.com/MeteoSwiss/publication-opendata/issues?q=is%3Aissue+sort%3Aupdated-desc).

> [!NOTE]
> All information in this repository reflects the current state of work and is subject to change.

### 1.2. Questions to the Open Data user community
These are the **current questions to the Open Data user community** on which we are asking for feedback:

| Data category | ID | Question | Status | Since date |
| :------------ | :- | :------- | :----- | :--------- |
| **Surface** | S1 | [Aggregated (calculated) maximum and minimum?](https://github.com/MeteoSwiss/publication-opendata/discussions/1) | Open for feedback | 2023-10-02 |
| **Surface** | S2 | [Multi-hour or multi-day aggregated sums?](https://github.com/MeteoSwiss/publication-opendata/discussions/22) | Open for feedback | 2023-10-02 |
| **Surface** | S3 | [Mutation information?](https://github.com/MeteoSwiss/publication-opendata/discussions/24) | Open for feedback | 2023-10-02 |
| **Surface** | S4 | [Metadata for stations and parameters?](https://github.com/MeteoSwiss/publication-opendata/discussions/27) | Open for feedback | 2023-10-02 |
| **Atmosphere** | A0 | no specific question yet | ... | ... |
| **Model** | M0 | no specific question yet | ... | ... |
| **Grid** | G0 | no specific question yet | ... | ... |

### 1.3. General contact point
If you have any questions, please contact the project team: [opendata(at)meteoswiss.ch](mailto:opendata@meteoswiss.ch)

## 2. Open Data products

### 2.1. Overview of data types to be made available as Open Data
MeteoSwiss operates an extensive monitoring network, both on the ground (surface stations) and in the atmosphere, that enables it to collect round-the-clock meteorological data for the whole of Switzerland. These data form the basis for making weather forecasts, issuing bad weather warnings, and analysing climate change. Furthermore MeteoSwiss operates a weather model for forecasting and also generates gridded data sets.

This is the **current status of the clarifications** as to which data types can be made available (and how) under an Open Data license by MeteoSwiss, and which not:

| Can be made available as Open Data | in clarification if/how | cannot be made available as Open Data - with reasons) | 
| :--------------------------------- | :---------------------- | :---------------------------------------------------- |
| [Automatic weather stations](https://github.com/MeteoSwiss/publication-opendata/tree/main#231-automatic-weather-stations-smn-smn-precip-smn-tower) | <!-- [Aerosol measurements](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/aerosol-measurements.html) --> | [Aviation weather](https://www.meteoswiss.admin.ch/services-and-publications/service/weather-and-climate-products/aviation-weather.html) - These data are collected on behalf of and financed by professional aviation |
| [Manual precipitation stations](https://github.com/MeteoSwiss/publication-opendata/tree/main#232-manual-precipitation-stations-nime-tot) |  |  |
| [Visual observations](https://github.com/MeteoSwiss/publication-opendata/tree/main#233-visual-observations-obs) |  |  |
| [Climate stations "Swiss NBCN"](https://github.com/MeteoSwiss/publication-opendata/tree/main#234-climate-stations-swiss-nbcn-nbcn-nbcn-precip) | [Records and extremes](https://github.com/MeteoSwiss/publication-opendata/tree/main#2341-records-and-extremes) |  |
| [Swiss pollen monitoring stations](https://github.com/MeteoSwiss/publication-opendata/tree/main#235-swiss-pollen-monitoring-stations-pollen) |  |  |
| [Phenological observations](https://github.com/MeteoSwiss/publication-opendata/tree/main#236-phenological-observations-phenology) |  |  |
| [Radio soundings](https://github.com/MeteoSwiss/publication-opendata/tree/main#241-radio-soundings-radiosounding) | [Windprofiler](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/windprofiler.html) | [Observations from aircraft](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/observations-from-aircraft.html) - Data does not belong to MeteoSwiss |
|  | [LIDAR and ceilometers](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/lidar-and-ceilometers.html) | [Satellite observations](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/satellite-observations.html) - Data does not belong to MeteoSwiss |
|  | [Microwave radiometry](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/microwave-radiometry.html) | [Lightning detection network](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/lightning-detection-network.html) - Data does not belong to MeteoSwiss |
|  | [Ozone measurements](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/ozone-measurements.html) |  |
|  | [Radiation monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/radiation-monitoring-network.html) |  |
| [INCA data (nowcasting)](https://github.com/MeteoSwiss/publication-opendata/tree/main#251-inca-data-nowcasting) |  |  |
| [COSMO/ICON data (forecasting)](https://github.com/MeteoSwiss/publication-opendata/tree/main#252-cosmoicon-data-forecasting) |  |  |
| [Postprocessed local forecast data (data4web)](https://github.com/MeteoSwiss/publication-opendata/tree/main#253-postprocessed-local-forecast-data-data4web) |  |  |
| [Spatial climate data](https://github.com/MeteoSwiss/publication-opendata/tree/main#261-Spatial-climate-data) |  |  |
| [Radar and CompiPrecip data](https://github.com/MeteoSwiss/publication-opendata/tree/main#262-Radar-and-combiprecip-data) |  |  |
|  | [Weather hazard data](https://www.meteoswiss.admin.ch/weather/hazards/hazard-map.html) - Warnings for severe weather (wind, thunderstorm, rain, snow, heat, frost, slippery roads) |  |

### 2.2. General information on the data

#### 2.2.1. Data granularity
For all types of data MeteoSwiss uses standard granularities. Depending on the application not all granularites are available. For measurement data the lowest granulartiy is usually called 'raw data' (Rohwert) or 'original data' (Originalwert). Higher granularities are called 'aggregations' or 'aggregated values'. The World Meteorological Organization (WMO) does issue guidelines on how national weather services have to aggregate values and MeteoSwiss does follow these guidelines.

If you need hourly, daily, monthly or yearly values, we strongly recommend that you download the according granularity. Downloading the raw data (10min) and calculating sums or means yourself, will not always lead to the same results! Furthermore for historic data it is possibly that manual data corrections have only been applied on higher granularities (like hourly or daily data), which means that historic raw data can still contain errors.

This is the overview of the granularities used by MeteoSwiss:

| Granularity | Name | Description | Used for |
| ----------- | ---- | ----------- | -------- |
| T | 10min value | At MeteoSwiss this is the standard granularity for realtime data of the automatic measurement network SwissMetNet (SMN) or the model output. Meteorological observations do also use this granularity but only offer values at fixed intervals like 6UTC, 12UTC and 18UTC (called "Terminwerte")! | [SMN](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html), [OBS](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-observation-network.html) |
| H | Hourly value | Either aggregated from 10min values or provided by the instrument/network | [Pollen](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) |
| D | Daily value | Used throughout the MeteoSwiss measurement network before automatization in 1981 started. Today still used for manual precipitation and snow measurements. For automatic stations daily values are calculated using 10min values according to WMO guidelines. | [NIME](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html) |
| M | Monthly value | Usually aggregated from daily values and widely used in climatology for homogenized data and norm values and for seasonal data. For some very old data series (pre 1864) only monthly data exists!| [Homogeneous data series](https://www.meteoswiss.admin.ch/climate/climate-change/changes-in-temperature-precipitation-and-sunshine/homogeneous-data-series-since-1864.html), [Climate normals](https://www.meteoswiss.admin.ch/climate/the-climate-of-switzerland/climate-normals.html) |
| Y | Yearly value | Usually aggregated from daily values and mostly used in climatology or climate change screnarios. | [Climate change scenarios](https://www.meteoswiss.admin.ch/climate/climate-change/swiss-climate-change-scenarios.html)|

#### 2.2.2. Data structure and update cycle
For measurement data MeteoSwiss provides an optimized directory structure separating older historical data, which is not updated regularly, and more recent data, which is updated more often. For realtime data we provide a third "now" directory with a high update frequency.

This is the overview:

| Type | Description | Update cycle | Used for |
| ---- | ----------- | ------------ | -------- |
| historical | From the start of the measurement until December 31st of last year | Once a year | [Granularity](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) M, D, H, T |
| recent | From January 1st of this year until yesterday | Daily at 12UTC | [Granularity](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) M, D, H, T |
| now | The most recent realtime data from yesterday 12UTC to now | Every 10min | Only [Granularity](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) H, T |
| `no type` | For certain data types this concept does not apply | varies | varies (e.g. [Granularity](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) Y) |

#### 2.2.3. Time stamps and time intervals
All reference time stamps at MeteoSwiss are in [UTC](https://www.utctime.net)! Depending on the granularity the time stamp does define different intervals:
- T: The sum, mean or max/min of the last 10 minutes (ReferenceTS 16:00 = `15:50:01 to 16:00:00`)
- H: The sum, mean or max/min of the last six 10min-values (ReferenceTS 16:00 = `15:10 to 16:00`). Please note: Hourly values before 2018 were calculated differently based on the SYNOP schedule (ReferenceTS 16:00 = `14:50 to 15:40`)! 
- D: For most parameters the sum, mean or max/min from 00:00 to 23:50 of the according date. Exception for precipitation and snow (manual measurement times used for consistency) where the interval is 6:00 UTC until 5:50 UTC tomorrow (ReferenceTS 22.6.2023 = `22.6.2023 6:10 UTC to 23.6.2023 6:00 UTC`)
- M: The sum, mean or max/min of the whole month from 1st to last day of month (ReferenceTS 1.6.2023 = `1.6.2023 00:10 UTC to 30.6.2023 24:00 UTC`)
- Y: The sum, mean or max/min of the whole year (ReferenceTS 1.1.2023 = `1.1.2023 00:10 UTC to 31.12.2023 24:00 UTC`)

**Accordingly, it follows that:**
- for granularity T and H the time stamp defines the end of the measurement interval and
- for higher granularities (D, M and Y) the time stamp defines the beginning of the interval!

#### 2.2.4. Column separators, decimal dividers and missing values
Generally, columns are separated with a semicolon (`;`). The decimal divider is a full stop (`.`). Missing values are indicated with a hyphen (`-`).

### 2.3. Surface data
MeteoSwiss operates a network of [land-based weather stations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations.html) where current weather and climate data are automatically recorded. It covers all parts of the country and all altitude levels. The measurements are supplemented with a wide array of additional observations, ranging from manual recording of cloud cover and vegetation development, to measurements of fine particulate matter, through to a network of cameras that covers all major sections of terrain and mountain passes in Switzerland.

All MeteoSwiss surface stations have a name and an identfier consisting of three letters (e.g. `BER` for [Bern / Zollikofen](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en&station=BER&chart=hour) or `LUG` for [Lugano](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en&station=LUG&chart=hour)). Data files use this station identifier in the file name throughout all directories. A list of all station identfiers with station names, coordinates, height etc. can be found in the according metadata section.

#### 2.3.1. Automatic weather stations (`smn`, `smn-precip`, `smn-tower`)
SwissMetNet, the [automatic measurement network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html) of MeteoSwiss, comprises about 160 automatic stations with a full measurement program (`smn`). These stations deliver a multitude of current data on weather and climate in Switzerland every ten minutes. The network is supplemented by around 100 automatic precipitation stations (`smn-precip`). Together, these stations form the basis for the creation of reliable local weather forecasts as well as severe weather and flood warnings. Additionally MeteoSwiss operates three tower stations at 150m to 230m above ground for boundry layer measurements (`smn-tower`). The time series can begin before the introduction of automatic measurements in 1981; the three manually measured values per day are stored as individual 10-minute values ("term values").

| *Dataset title*                | Measurement data from automatic weather stations |
| :----------------------------- | :----------------------------------------------- |
| *Data structure*               | see example files: [`smn`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn), [`smn-precip`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn-precip), [`smn-tower`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn-tower) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `T`, `H`, `D`, `M` and `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`), daily (`recent`) or hourly (`now`) |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | ≤5.3 MB |
| *Visualisation*                | [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv) |
| *Parameter metadata*           | see parameter files: [`smn-T`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-T.csv), [`smn-H`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-H.csv), [`smn-D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-D.csv), [`smn-M`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-M.csv) and [`smn-Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-Y.csv)
| *Additional remarks*           | One file per station. |

#### 2.3.2. Manual precipitation stations (`nime`, `tot`)
In addition to its automatic precipitation measurements, MeteoSwiss operates a [manual precipitation monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html). Measurements are taken once a day and transmitted to MeteoSwiss via SMS. The network comprises 243 locations, 190 stations measure rainfall and snow, and 53 stations measure snow only (`nime`). Due to their long-series measurements, they are of great climatological significance. In mountainous areas that are difficult to access, around 57 totalisers are used which record the volume of precipitation for an entire year (`tot`).

| *Dataset title*                | Measurement data from manual precipitation stations |
| :----------------------------- | :-------------------------------------------------- |
| *Data structure*               | see example files: [`nime`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/manual-precipitation-stations-nime), [`tot`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/manual-precipitation-stations-tot) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`), daily (`recent`) or hourly (`now`) |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | ≤0.6 MB |
| *Visualisation*                | [NIME and TOT network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-manuell&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-manuell/ch.meteoschweiz.messnetz-manuell_en.csv) |
| *Parameter metadata*           | see parameter files: [`nime-D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-nime-D.csv), [`nime-M`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-nime-M.csv), [`nime-Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-nime-Y.csv) and [`tot-Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-tot-Y.csv) |
| *Additional remarks*           | One file per station. |

#### 2.3.3. Visual observations (`obs`)
The information on current weather events is supplemented by [visual human observations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-observation-network.html). The atmospheric conditions around the observation site are described in detail.

| *Dataset title*                | Measurement data from visual observations |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example files: [`obs`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/visual-observations-obs) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `T` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`), daily (`recent`) or hourly (`now`) |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | ≤0.04 MB |
| *Visualisation*                | [OBS network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-manuell&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-beobachtungen/ch.meteoschweiz.messnetz-beobachtungen_en.csv) |
| *Parameter metadata*           | see parameter file: [`obs-T`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-obs-T.csv) |
| *Additional remarks*           | One file per station. |

#### 2.3.4. Climate stations "Swiss NBCN" (`nbcn`, `nbcn-precip`)
The [Swiss National Basic Climatological Network "Swiss NBCN"](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/swiss-national-basic-climatological-network.html) connects the major ground-based stations within the MeteoSwiss monitoring network. It consists of 29 climate monitoring stations and 46 precipitation stations. The measurement series available in digital form for temperature, precipitation and hours of sunshine date back, in some cases, to the mid-nineteenth century. The measurement series are [homogenised](https://www.meteoschweiz.admin.ch/klima/klimawandel/entwicklung-temperatur-niederschlag-sonnenschein/homogene-messreihen-ab-1864.html). Homogenised time series from other weather stations are also provided.

| *Dataset title*                | Measurement data from the Swiss National Basic Climatological Network |
| :----------------------------- | :-------------------------------------------------------------------- |
| *Data structure*               | see example files: [`nbcn`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/climate-stations-swiss-nbcn-climate), [`nbcn-precip`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/climate-stations-swiss-nbcn-climate-precip) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`), daily (`recent`) or hourly (`now`) |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | ≤0.9 MB |
| *Visualisation*                | [CLIMATE network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-klima&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-klima/ch.meteoschweiz.messnetz-klima_en.csv) |
| *Parameter metadata*           | see parameter files: [`nbcn-D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-climate-D.csv), [`nbcn-M`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-climate-M.csv) and [`nbcn-Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-climate-Y.csv) |
| *Additional remarks*           | One file per station. |

<!-- ##### 2.3.4.1 Records and extremes
Additionally the top 10 records of every climate station and the overall records can be downloaded per parameter separately.

| *Dataset title*                | ... |
| :----------------------------- | :----------------------------- |
| *Data structure*               | see example file: [`...`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/...) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`) |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | ... (MB/GB/TB) |
| *Visualisation*                | [...](...) |
| *Station metadata*             | see [station list (CSV)](...) |
| *Parameter metadata*           | see parameter file: [`...-Y`]() |
| *Additional remarks*           | One file per station. | -->

#### 2.3.5. Swiss pollen monitoring stations (`pollen`)
MeteoSwiss operates the [national pollen monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/pollen-monitoring-network-manual-method.html). This consists of 14 monitoring stations which cover Switzerland's most important climatic and vegetation regions. The measurements obtained provide invaluable information for those who suffer from allergies. Additionally since 2023 the new [automatic pollen network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) is operational: for the first time in the world, instead of daily averages being available after a week, information is available in real time at an hourly resolution.

| *Dataset title*                | Measurement data from the Swiss Pollen Monitoring Network |
| :----------------------------- | :-------------------------------------------------------- |
| *Data structure*               | see example files: [`pollen`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/swiss-pollen-monitoring-stations-pollen) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `H`, `D`, `M` and `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`), daily (`recent`) or hourly (`now`) |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | 0.6 MB |
| *Visualisation*                | [POLLEN network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-pollen&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-pollen/ch.meteoschweiz.messnetz-pollen_en.csv) |
| *Parameter metadata*           | see parameter files: [`pollen-H`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-pollen-H.csv) and [`pollen-D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-pollen-D.csv) |
| *Additional remarks*           | One file per station. |

#### 2.3.6. Phenological observations (`phenology`)
The [Swiss Phenology Network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/swiss-phenology-network.html) consists of 160 stations. Some 26 different plant species are observed in order to describe the vegetation development. On the basis of this information, it is possible to investigate the impact of climate change on the vegetation. The observations also serve to generate forecasting models for the start of flowering.

| *Dataset title*                | Measurement data from the Swiss Phenology Network |
| :----------------------------- | :-------------------------------------------------------- |
| *Data structure*               | see example files: [`phenology`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/phenology) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`) or daily (`recent`) |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | ≤7.1 MB |
| *Visualisation*                | [PHENOLOGY network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-phaenologie&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-phaenologie/ch.meteoschweiz.messnetz-phaenologie_en.csv) |
| *Parameter metadata*           | see parameter file: [`phenology-Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-phenology-Y.csv) |
| *Additional remarks*           | One file for all stations. |

### 2.4. Atmosphere data
MeteoSwiss obtains relevant data for weather forecasting and climate analysis from the [atmosphere](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere.html). The properties and composition of the atmosphere are studied using various instruments and methods, including weather balloons, satellites and laser equipment. Weather radar stations play an important role, as they record precipitation and thunderstorms throughout Switzerland in real time.

#### 2.4.1. Radio soundings (`radiosounding`)
MeteoSwiss performs soundings twice a day using weather balloon radiosondes. This allows important meteorology-related atmospheric values to be measured at high altitudes. The results of the latest [radio soundings](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/radio-soundings.html) are made available in the form of data files ([decoded data](https://www.meteoswiss.admin.ch/services-and-publications/applications/radio-soundings.html#tab=radio-soundings-decoded)) and graphs ([emagrams](https://www.meteoswiss.admin.ch/services-and-publications/applications/radio-soundings.html#tab=radio-soundings-emagram)).

The radiosondes measure air pressure, temperature and humidity. Attached to a [weather balloon](https://www.meteoswiss.admin.ch/weather/weather-and-climate-from-a-to-z/weather-balloon.html) and carried high into the atmosphere, the radiosonde also records the exact position, allowing altitude, wind speed and direction to be determined. The data obtained in this way are of great importance for weather forecasts and climate research. MeteoSwiss launches a weather balloon twice a day from the sounding station in Payerne. Special soundings are also carried out to determine other parameters such as ozone or aerosol concentrations. In addition, MeteoSwiss operators launch research flights, for which several radiosondes are attached to the same balloon. This allows the readings to be compared with each other, checked for quality and verified.

| *Dataset title*                | Atmosphere data from radio sounding station Payerne |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [`radiosounding`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-atmosphere/radiosounding) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `T` |
| *Update frequency*             | 12h (00h, 12h UTC) |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | 0.02 MB |
| *Visualisation*                | [Emagram](https://www.meteoswiss.admin.ch/services-and-publications/applications/radio-soundings.html#tab=radio-soundings-emagram) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-atmosphaere/ch.meteoschweiz.messnetz-atmosphaere_en.csv) |
| *Parameter metadata*           | see [parameter file](https://github.com/MeteoSwiss/publication-opendata/blob/main/atmosphere/radiosounding-PAY-metadata) |
| *Additional remarks*           | One file per station. |

### 2.5. Model data

<!-- Jump directly to 2.5.2. [COSMO/ICON data (forecasting)](https://github.com/MeteoSwiss/publication-opendata/tree/main#252-cosmoicon-data-forecasting). <br> -->
> Jump directly to 2.5.3. [Postprocessed local forecast data (data4web)](https://github.com/MeteoSwiss/publication-opendata/tree/main#253-postprocessed-local-forecast-data-data4web). <br>

#### 2.5.1. INCA data (nowcasting)
The INCA [nowcasting](https://www.meteoswiss.admin.ch/weather/warning-and-forecasting-systems/nowcasting.html) forecasts come in 2 versions for most parameters a) a short 0h- +6h version and an b) an extended 6h-+28/33h version.
Please be aware, that in the extended versions, the part after the first 6h comes from the COSMO-1E model, which means, that it is beeing updated only every 3h (00h, 03h, 06h, 09h etc. UTC). Only the first +6h are beeing updated according to the respective update frequency. 
For more information see the metadata in each NetCDF-File.

> Jump directly 2.5.1.1. [INCA precipitation - quantitative/qualitative](https://github.com/MeteoSwiss/publication-opendata/tree/main#2511-inca-precipitation---quantitativequalitative). <br>
> Jump directly 2.5.1.2. [INCA precipitation type - rain, snow, snow-rain, freezing rain, rain&hail](https://github.com/MeteoSwiss/publication-opendata/tree/main#2512-inca-precipitation-type---rain-snow-snow-rain-freezing-rain-rainhail). <br>
> Jump directly 2.5.1.3. [INCA snowfall - quantitative/qualitative](https://github.com/MeteoSwiss/publication-opendata/tree/main#2513-inca-snowfall---quantitativequalitative). <br>
> Jump directly 2.5.1.4. [INCA snow accumulation & snowfall line](https://github.com/MeteoSwiss/publication-opendata/tree/main#2514-inca-snow-accumulation--snowfall-line). <br>
> Jump directly 2.5.1.5. [INCA temperature](https://github.com/MeteoSwiss/publication-opendata/tree/main#2515-inca-temperature). <br>
> Jump directly 2.5.1.6. [INCA relative sunshine duration](https://github.com/MeteoSwiss/publication-opendata/tree/main#2516-inca-relative-sunshine-duration). <br>

##### 2.5.1.1. INCA precipitation - quantitative/qualitative
| *Dataset title*                | INCA precipitation quantitative (based on CombiPrecip, RR) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [RR_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/RR_INCA_202106280700.nc) |
| *Data granularity*             | Every 10min |
| *Update frequency*             | Every 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 1.7 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA precipitation quantitative extended forecast (based on CombiPrecip, RR_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version example file: [RR_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/RR_INCA_202106280700.nc) |
| *Data granularity*             | Every 10min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 20 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA precipitation qualitative (based on radar only, RP) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [RP_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/RP_INCA_202106280700.nc) |
| *Data granularity*             | Every 5min |
| *Update frequency*             | Every 5min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 3.1 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA precipitation qualitative extended forecast (based on radar only, RP_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version example file: [RP_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/RP_INCA_202106280700.nc) |
| *Data granularity*             | Every 5min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 37 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.5.1.2. INCA precipitation type - rain, snow, snow-rain, freezing rain, rain&hail
| *Dataset title*                | INCA precipitation type for RR in 5 classes rain, snow, snow-rain, freezing rain, rain&hail (hail first 30min only, PT) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [PT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/PT_INCA_202106280700.nc) |
| *Data granularity*             | Every 10min |
| *Update frequency*             | Every 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.7 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA precipitation type for RR_ext extended forecast in 5 classes rain, snow, snow-rain, freezing rain, rain&hail (hail first 30min only, PT_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version example file: [PT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/PT_INCA_202106280700.nc) |
| *Data granularity*             | Every 10min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 4.5 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA precipitation type for RP in 5 classes rain, snow, snow-rain, freezing rain, rain&hail (hail first 30min only, NT) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [NT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/NT_INCA_202106280700.nc) |
| *Data granularity*             | Every 5min |
| *Update frequency*             | Every 5min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 1.4 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA precipitation type for RP_ext extended forecast in 5 classes rain, snow, snow-rain, freezing rain, rain&hail (hail first 30min only, NT_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version see example file: [NT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/NT_INCA_202106280700.nc) |
| *Data granularity*             | Every 5min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 8.5 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.5.1.3. INCA snowfall - quantitative/qualitative
| *Dataset title*                | INCA Snowfall quantitative (based on CombiPrecip, RS) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [RS_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/RS_INCA_202106280700.nc) |
| *Data granularity*             | Every 10min |
| *Update frequency*             | Every 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.4 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Snowfall quantitative extended forecast (based on CombiPrecip, RS_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version example file: [RS_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/RS_INCA_202106280700.nc) |
| *Data granularity*             | Every 10min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 1.5 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Snowfall qualitative (based on radar only, PN) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [PN_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/PN_INCA_202106280700.nc) |
| *Data granularity*             | Every 5min |
| *Update frequency*             | Every 5min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.6 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Snowfall qualitative extended forecast (based on radar only, PN_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version example file: [PN_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/PN_INCA_202106280700.nc) |
| *Data granularity*             | Every 5min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 2.9 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.5.1.4. INCA snow accumulation & snowfall line
| *Dataset title*                | INCA New Snow Accumulation 24h (SH_BK_24) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [SH_BK_24_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/SH_BK_24_INCA_202106280700.nc) |
| *Data granularity*             | 24h |
| *Update frequency*             | 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.04 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Snowfall line (ZS) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [ZS_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/ZS_INCA_202106280700.nc) |
| *Data granularity*             | 60min |
| *Update frequency*             | 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 12.2 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.5.1.5. INCA temperature
| *Dataset title*                | INCA Zero degree isotherm (Z0) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [Z0_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/Z0_INCA_202106280700.nc) |
| *Data granularity*             | 60min |
| *Update frequency*             | 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 12.2 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA temperature (TT) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [TT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/TT_INCA_202106280700.nc) |
| *Data granularity*             | 60min |
| *Update frequency*             | 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 12.2 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Temperature extended (TT_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version example file: [TT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/TT_INCA_202106280700.nc) |
| *Data granularity*             | 60min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 42 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Dewpoint temperature (TD) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [TD_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/TD_INCA_202106280700.nc) |
| *Data granularity*             | 60min |
| *Update frequency*             | 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 12.2 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Dewpoint temperature Extended (TD_Ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version example file: [TD_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/TD_INCA_202106280700.nc) |
| *Data granularity*             | 60min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | ... |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Soil surface temperature (TG) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [TG_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/TG_INCA_202106280700.nc) |
| *Data granularity*             | 60min |
| *Update frequency*             | 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 12.5 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.5.1.6. INCA relative sunshine duration
| *Dataset title*                | INCA Relative sunshine duration (SU) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [SU_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/SU_INCA_202106280700.nc) |
| *Data granularity*             | 10min |
| *Update frequency*             | 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 6.4 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

#### 2.5.2. COSMO/ICON data (forecasting)
The COSMO/ICON [forecasting](https://www.meteoswiss.admin.ch/weather/warning-and-forecasting-systems/nowcasting.html) systems calculate future atmospheric conditions. MeteoSwiss uses the COSMO (Consortium for Small-scale Modeling) numerical weather forecasting model for the production of regional and local forecast products in the topographically challenging Alpine region. In order to be able to provide optimal probability forecasts for as many uses as possible, MeteoSwiss deploys two different ensemble configurations of COSMO: COSMO-1E and COSMO-2E. Together with the [ECMWF forecasts](https://www.ecmwf.int/en/forecasts), these form the basis for the daily weather forecasts produced by MeteoSwiss, as well as warnings of extreme weather conditions such as storms and precipitation events.

Several times a day, COSMO-1E and COSMO-2E calculate different forecasts respectively (known as “members”), each with slightly different initial conditions: 
- COSMO-1E comprises an ensemble of 11 forecasts at a resolution of 1.1 km, calculated eight times a day for central and southern Europe.
- COSMO-2E is calculated four times a day from 21 realisations at a resolution of 2.2 km. 

From this collection of forecasts, the “ensemble”, the probability of a certain weather event occurring can be calculated. The ensemble also provides a measure of the predictability of the expected weather situation and thus also an estimate for the forecast reliability. **The data are available from these individual forecasts. In addition, derived values such as quantiles can also be ordered.**

**Using the numerical weather forecast models COSMO-1E and COSMO-2E, MeteoSwiss offers direct model outputs for the entire Alpine region in the form of hourly analyses or forecasts for up to five days ahead. Forecasts for the whole of Switzerland or the entire Alpine region are available for a wide range of parameters.**

The MeteoSwiss forecast data (e.g. for parameters such as temperature, humidity, precipitation, wind, air pressure, geopotential, evaporation and radiation) can be obtained in numerous formats:
- **Horizontal fields: Data and graphics for the whole model domain or for a section that covers the whole of Switzerland.**
- **Tables with all the main weather variables at any number of locations within the model domain. Supplied in CSV format, the data can be integrated into the customer’s own data processing systems.
Meteograms with graphs of the main parameters for a particular location.**

**In principle, all of the parameters used in the local forecast on the website and in the MeteoSwiss App are available.** Supplied in CSV format, the data can be integrated into the customer’s own data processing systems:
- [Example of data (**other formats available on request**) (ZIP, 2.5 MB)](https://www.meteoswiss.admin.ch/dam/jcr:2e18893b-49dc-418c-ba51-9a2b6d81f739/Datenbeispiel-cosmo-2e.zip)
- [**Examples of probabilistic products**](https://www.meteoswiss.admin.ch/weather/warning-and-forecasting-systems/cosmo-forecasting-system/examples-of-probabilistic-products.html)

#### 2.5.3. Postprocessed local forecast data (data4web)
The postprocessed forecast data is based on a [mix of different models](https://www.meteoswiss.admin.ch/services-and-publications/service/weather-and-climate-products/weather-forecasts.html) (INCA, COSMO-1E, COSMO-E2, ECMWF) and is available for all ZIP-codes, [SMN](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html)-stations and selected POI in the mountains as point data. 
The forecast is available for the time period from +0h to +192h and is being updated hourly. 
It is the same forecast data used in the MeteoSwiss app and on the website for each ZIP-code. 

For each parameter there is a single file. Here we provide only a few parameters for review. 

As for the geolocation of the data, the following metadata-files are being provided for mapping of the data: 
- ZIP-code locations [Data4Web_legend_PLZ.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessed-local-forecast-data-data4web/blob/main/Data4Web_Legend_PLZ.csv)
- SMN-stations and POI locations [Data4Web_legend_POI_Stations.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessed-local-forecast-data-data4web/blob/main/Data4Web_Legend_POI_Stations.csv)

##### 2.5.3.1. Local forecast precipitation
| *Dataset title*                | Hourly precipitation sum |
| :----------------------------- | :------------------------- |
| *Data structure*               | see example file (zipped CSV): [VNUT12.LSSX.202309271300.rre150b0.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessed-local-forecast-data-data4web/blob/main/VNUT12.LSSX.202309271300.rre150b0.zip) |
| *Data granularity*             | hourly |
| *Update frequency*             | hourly |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | 29.9 MB (unzipped) |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | unit: `mm` or `l/m2` |

##### 2.5.3.2. Local forecast temperature
| *Dataset title*                | Hourly average temperature |
| :----------------------------- | :------------------------- |
| *Data structure*               | see example file (zipped CSV): [VNUT12.LSSX.202309271300.tre200b0.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessed-local-forecast-data-data4web/blob/main/VNUT12.LSSX.202309271300.tre200b0.zip) |
| *Data granularity*             | hourly |
| *Update frequency*             | hourly |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | 31.6 MB (unzipped) |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | unit: `°C` |

| *Dataset title*                | Daily Temperature minimum |
| :----------------------------- | :------------------------- |
| *Data structure*               | see example file: [VNUT12.LSSX.202309271300.tre200dn.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessed-local-forecast-data-data4web/blob/main/VNUT12.LSSX.202309271300.tre200dn.csv) |
| *Data granularity*             | hourly |
| *Update frequency*             | hourly |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | 0.2 MB (unzipped) |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | unit: `°C` |

| *Dataset title*                | Daily temperature maximum |
| :----------------------------- | :------------------------- |
| *Data structure*               | see example file: [VNUT12.LSSX.202309271300.tre200dx.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessed-local-forecast-data-data4web/blob/main/VNUT12.LSSX.202309271300.tre200dx.csv) |
| *Data granularity*             | hourly |
| *Update frequency*             | hourly |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | 0.2 MB |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | unit: `°C` |

##### 2.5.3.2. Local forecast sunshine duration
| *Dataset title*                | Hourly sunshine duration |
| :----------------------------- | :------------------------- |
| *Data structure*               | see example file (zipped CSV): [VNUT12.LSSX.202309271300.spr100h0.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessed-local-forecast-data-data4web/blob/main/VNUT12.LSSX.202309271300.spr100h0.zip) |
| *Data granularity*             | hourly |
| *Update frequency*             | hourly |
| *Format*                       | [`CSV`](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values) |
| *Volume*                       | 30.9 MB (unzipped) |
| *Parameter metadata*           | see example file |
| *Additional remarks*           | unit: `minutes` |

### 2.6. Grid data

#### 2.6.1. Spatial climate data  
Spatial climate data are statistically derived from surface data. Those spatial climate data, which contain radiation and cloud cover parameters, are derived from MeteoSat satellite data together with surface data. See the [overview of spatial climate products (PDF)](https://www.meteoschweiz.admin.ch/dam/jcr:215c313a-dc13-4b67-bca0-dbd966597f9a/ProdDoc_Cover-dfie.pdf). Frr each product see the "detailed product document(s)" below for further information, and the parameter metadata in each example file.

##### 2.6.1.1. Surface derived grid data
| *Dataset title*                | Gridded precipitation data (RprelimD, RhiresD, RhiresM, RhiresY) |
| :----------------------------- | :----------------------------------------------- |
| *Detailed product documents*   | RprelimD: [Daily Precipitation (preliminary analysis)](https://www.meteoswiss.admin.ch/dam/jcr:86ca15d3-2b56-4753-84fb-135e40d6a5a1/ProdDoc_RprelimD.pdf) <br> RhiresD: [Daily Precipitation (final analysis)](https://www.meteoswiss.admin.ch/dam/jcr:4f51f0f1-0fe3-48b5-9de0-15666327e63c/ProdDoc_RhiresD.pdf) <br> RhiresM, RhiresY: [Monthly and Yearly Precipitation](https://www.meteoswiss.admin.ch/dam/jcr:d4f53a4a-d7f4-4e1e-a594-8ff4bfd1aca5/ProdDoc_RhiresM.pdf) <br> |
| *Data structure*               | see example files: [RhiresD.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/RhiresD_ch01h.swiss.lv95_202305010000_202305310000.nc), [RhiresM.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/RhiresM_ch01r.swiss.lv95_202305010000_202305010000.nc), [RhiresY.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/RhiresY_ch01r.swiss.lv95_202201010000_202201010000.nc) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| *Update frequency*             | according to granularity |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 1.1 MB for individual files, monthly files with daily data 13 MB |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | Gridded temperature data (TabsD, TminD, TmaxD, TabsM, TminM, TmaxM, TabsY, TminY, TmaxY) |
| :----------------------------- | :----------------------------------------------- |
| *Detailed product documents*   | TabsD, TminD, TmaxD: [Daily Mean, Minimum and Maximum Temperature](https://www.meteoswiss.admin.ch/dam/jcr:818a4d17-cb0c-4e8b-92c6-1a1bdf5348b7/ProdDoc_TabsD.pdf) <br> TabsM, TabsY: [Monthly and Yearly Mean Temperature](https://www.meteoswiss.admin.ch/dam/jcr:33e26211-9937-4f80-80a3-09cfe54663bc/ProdDoc_TabsM.pdf) <br> |
| *Data structure*               | see example files: [TabsD.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/TabsD_ch01r.swiss.lv95_202305010000_202305310000.nc), [TabsM.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/TabsM_ch01r.swiss.lv95_202305010000_202305010000.nc), [TmaxM.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/TmaxM_ch01r.swiss.lv95_202305010000_202305010000.nc), [TminY.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/TminY_ch01r.swiss.lv95_202201010000_202201010000.nc) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| *Update frequency*             | according to granularity |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 1.1 MB for individual files, monthly files with daily data 13 MB |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | Gridded relative sunshine duration data (SreldD, SrelM, SrelY) |
| :----------------------------- | :----------------------------------------------- |
| *Detailed product documents*   | SrelD: [Daily Relative Sunshine Duration](https://www.meteoswiss.admin.ch/dam/jcr:981891db-30d1-47cc-a2e1-50c270bdaf22/ProdDoc_SrelD.pdf) <br> SrelM, SrelY: [Monthly and Yearly Relative Sunshine Duration](https://www.meteoswiss.admin.ch/dam/jcr:94421f3c-47f3-46fa-9939-1d494a0ce5fe/ProdDoc_SrelM.pdf) <br> |
| *Data structure*               | see example files: [SrelD.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/SrelD_ch01r.swiss.lv95_202305010000_202305310000.nc), [SrelM.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/SrelM_ch01r.swiss.lv95_202305010000_202305010000.nc), [SrelY.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/SrelY_ch01r.swiss.lv95_202201010000_202201010000.nc) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| *Update frequency*             | according to granularity |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 1.1 MB for individual files, monthly files with daily data 13 MB |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.6.1.2. Satellite derived grid data

| *Dataset title*                | Gridded global radiation (MSG.SIS.D, MSG.SIS.M, MSG.SIS.Y) |
| :----------------------------- | :----------------------------------------------- |
| *Detailed product documents*   | MSG.SIS.D, MSG.SIS.M, MSG.SIS.Y: [Daily, monthly and yearly satellite-based global radiation](https://www.meteoswiss.admin.ch/dam/jcr:b0bbcbac-1a17-481b-aea4-e87e56183613/ProdDoc_SIS.pdf) <br> |
| *Data structure*               | see example files: [MSG.SIS.D.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SIS.D_ch02.lonlat_20201206000000.nc), [MSG.SIS.M.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SIS.M_ch02.lonlat_20210401000000.nc), [MSG.SIS.Y.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SIS.Y_ch02.lonlat_20210101000000.nc) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| *Update frequency*             | according to granularity |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.1 MB |
| *Additional remarks*           | Coordinate System: WGS84 lat/lon EPSG:4326 |

| *Dataset title*                | Gridded diffuse radiation (MSG.SISDIF.D, MSG.SISDIF.M, MSG.SISDIF.Y) |
| :----------------------------- | :----------------------------------------------- |
| *Detailed product documents*   | MSG.SISDIF.D, MSG.SISDIF.M, MSG.SISDIF.Y: [Daily, monthly and yearly satellite-based global radiation](https://www.meteoswiss.admin.ch/dam/jcr:b0bbcbac-1a17-481b-aea4-e87e56183613/ProdDoc_SIS.pdf) <br> |
| *Data structure*               | see example files: [MSG.SISDIF.D.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SISDIF-No-Horizon.D_ch02.lonlat_20201206000000.nc), [MSG.SISDIF.M.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SISDIF-No-Horizon.M_ch02.lonlat_20200401000000.nc), [MSG.SISDIF.Y.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SISDIF-No-Horizon.Y_ch02.lonlat_20200101000000.nc) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| *Update frequency*             | according to granularity |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.1 MB |
| *Additional remarks*           | Coordinate System: WGS84 lat/lon EPSG:4326 |

| *Dataset title*                | Gridded direct radiation (MSG.SISDIR.D, MSG.SISDIR.M, MSG.SISDIR.Y) |
| :----------------------------- | :----------------------------------------------- |
| *Detailed product documents*   | MSG.SISDIR.D, MSG.SISDIR.M, MSG.SISDIR.Y: [Daily, monthly and yearly satellite-based global radiation](https://www.meteoswiss.admin.ch/dam/jcr:b0bbcbac-1a17-481b-aea4-e87e56183613/ProdDoc_SIS.pdf) <br> |
| *Data structure*               | see example files: [MSG.SISDIR.D.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SISDIR.D_ch02.lonlat_20201206000000.nc), [MSG.SISDIR.M.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SISDIR.M_ch02.lonlat_20210401000000.nc), [MSG.SISDIR.Y.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SISDIR.Y_ch02.lonlat_20210101000000.nc) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| *Update frequency*             | according to granularity |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.1 MB |
| *Additional remarks*           | Coordinate System: WGS84 lat/lon EPSG:4326 |

| *Dataset title*                | Gridded cloud fractional cover (MSG.CFC.D, MSG.CFC.M, MSG.CFC.Y) |
| :----------------------------- | :----------------------------------------------- |
| *Detailed product documents*   | MSG.CFC.D, MSG.CFC.M, MSG.CFC.Y: [Daily, monthly and yearly satellite-based Cloud Fractional Cover](https://www.meteoswiss.admin.ch/dam/jcr:af0c491c-4bfc-4efd-bcee-5d019004afd1/ProdDoc_CFC.pdf) <br> |
| *Data structure*               | see example files: [MSG.CFC.D.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.CFC.D_ch02.lonlat_20201206000000.nc), [MSG.CFC.M.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.CFC.M_ch02.lonlat_20210401000000.nc), [MSG.CFC.Y.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.CFC.Y_ch02.lonlat_20210101000000.nc) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| *Update frequency*             | according to granularity |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.1 MB |
| *Additional remarks*           | Coordinate System: WGS84 lat/lon EPSG:4326 |

#### 2.6.2. Radar and CombiPrecip data
Supplementing the conventional precipitation measurements taken at ground level meteorological stations, MeteoSwiss operates a network of five weather radar stations which record every type of precipitation and storms in real time, are fully automated and, between them, cover the whole of Switzerland.

The sites are
- Albis near Zurich (equipped with the latest technology (dual polarisation) in 2012, monitors the atmosphere of the whole of northern Switzerland)
- Monte Lema in the Canton of Ticino (equipped with the latest technology (dual polarisation) in 2011, monitors the atmosphere of the whole of southern Switzerland)
- La Dôle near Geneva (equipped with the latest technology (dual polarisation) in 2011)
- Pointe de la Plaine Morte in the Canton of Valais (equipped with the latest technology (dual polarisation), commenced operation in 2014 and monitors the atmosphere in the inner Alpine region)
- the Weissfluhgipfel in the Canton of Graubünden (equipped with the latest technology (dual polarisation), commenced operation in 2016, and monitors the atmosphere in the inner Alpine region)

Radar and CombiPrecip data is being provided as [`HDF5`](https://hdfgroup.github.io/hdf5/_getting_started.html) which is the common exchange format for radar data.
See the metadata in each HDF5-File for further information. 
The radar data are divided into [Basic radar](https://www.meteoswiss.admin.ch/services-and-publications/service/weather-and-climate-products/basic-radar-products.html), [Advanced radar](https://www.meteoswiss.admin.ch/services-and-publications/service/weather-and-climate-products/radard-avanced.html) and [CombiPrecip](https://www.meteoswiss.admin.ch/dam/jcr:2691db4e-7253-41c6-a413-2c75c9de11e3/ProdDoc_CPC.pdf).

##### 2.6.2.1. Basic radar data

| *Dataset title*                | Precip (RZC) |
| :----------------------------- | :----------------------------------------------- |
| *Data structure*               | see example file: [RZC232371930VL.001.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/RZC232371930VL.001.h5) |
| *Data granularity*             | 5min |
| *Update frequency*             | according to granularity |
| *Format*                       | [`HDF5`](https://hdfgroup.github.io/hdf5/_getting_started.html) |
| *Volume*                       | 0.2 MB |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | MAX-ECHO (CZC) |
| :----------------------------- | :----------------------------------------------- |
| *Data structure*               | see example file: [CZC232371930VL.801.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/CZC232371930VL.801.h5) |
| *Data granularity*             | 5min |
| *Update frequency*             | according to granularity |
| *Format*                       | [`HDF5`](https://hdfgroup.github.io/hdf5/_getting_started.html) |
| *Volume*                       | 0.2 MB |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | ECHO TOP 15dBZ (EZC) |
| :----------------------------- | :----------------------------------------------- |
| *Data structure*               | see example file: [EZC232371930VL.815.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/EZC232371930VL.815.h5) |
| *Data granularity*             | 5min |
| *Update frequency*             | according to granularity |
| *Format*                       | [`HDF5`](https://hdfgroup.github.io/hdf5/_getting_started.html) |
| *Volume*                       | 0.1 MB |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | ECHO TOP 45dBZ (EZC) |
| :----------------------------- | :----------------------------------------------- |
| *Data structure*               | see example file: [EZC232371930VL.845.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/EZC232371930VL.845.h5) |
| *Data granularity*             | 5min |
| *Update frequency*             | according to granularity |
| *Format*                       | [`HDF5`](https://hdfgroup.github.io/hdf5/_getting_started.html) |
| *Volume*                       | 0.1 MB |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.6.2.2. Advanced radar data

| *Dataset title*                | Probability of Hail (POH) |
| :----------------------------- | :----------------------------------------------- |
| *Data structure*               | see example file: [BZC232371930VL.845.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/BZC232371930VL.845.h5) |
| *Data granularity*             | 5min |
| *Update frequency*             | according to granularity |
| *Format*                       | [`HDF5`](https://hdfgroup.github.io/hdf5/_getting_started.html) |
| *Volume*                       | 0.2 MB |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | Maximum Expected Severe Hail Size (MESHS) |
| :----------------------------- | :----------------------------------------------- |
| *Data structure*               | see example file: [MZC232371930VL.850.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/MZC232371930VL.850.h5) |
| *Data granularity*             | 5min |
| *Update frequency*             | according to granularity |
| *Format*                       | [`HDF5`](https://hdfgroup.github.io/hdf5/_getting_started.html) |
| *Volume*                       | 0.2 MB |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.6.2.3. CombiPrecip data

| *Dataset title*                | CombiPrecip (CPC) |
| :----------------------------- | :----------------------------------------------- |
| *Data structure*               | see example file: [CPC2335513304_00060.001.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/CPC2335513304_00060.001.h5) |
| *Data granularity*             | 60min (1h accumulation) |
| *Update frequency*             | 10min |
| *Format*                       | [`HDF5`](https://hdfgroup.github.io/hdf5/_getting_started.html) |
| *Volume*                       | 0.3 MB |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

### 2.7. Warning data
In clarification if/how can be made available as open data.

<!-- ## 3. Roadmap of MeteoSwiss' OGD service
In preparation ...

https://app.productplan.com/G_PR7ExN/views/1164487/?layout=timeline -->
