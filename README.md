# OGD@MeteoSwiss - Open Government Data

## Context and mission ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/context-and-purpose-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/context-and-purpose-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/context-and-purpose-IT))
In order to legally implement the [Federal Act on the use of electronic means for the performance of official duties' (EMBAG)](https://www.meteoswiss.admin.ch/about-us/remit-and-legal-mandate.html) the overall revision of the Ordinance on Meteorology and Climatology (MetV; SR 429.11) is now pending. In the current year (2023) the necessary technical and organizational measures for the implementation of OGD at MeteoSwiss are being tackled within the scope of a project.

### 1.1. Purpose of this repository
This repository is used by MeteoSwiss to inform potential users interested in open data about the plans and to receive specific feedback from them on proposals. **We describe below the open data products being designed by the various interdisciplinary data teams.** That is: the **data structures, formats, denominations, update frequencies, volumes and other specifics.**

All information reflects the current state of work and is subject to change. Finding out, collecting, analysing and weighting user needs is the central way for MeteoSwiss to be able to offer good open data products.

Thank you very much for your attention and openness to enter into an exchange with us for this purpose.

### 1.2. General contact point
If you have any questions, please contact the project core team: [opendata(at)meteoswiss.ch](mailto:opendata@meteoswiss.ch)

## Open data products ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/opendata-products-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/opendata-products-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/opendata-products-IT))

<!-- Tabelle mit 4 sprachen in spalten, statt Übersetzungen in Files? -->

- publication-opendata
     - [surface](https://github.com/MeteoSwiss/publication-opendata/tree/master#21-surface)
        - ~~aviation~~
        - [smn (automatic-measurements)](https://github.com/MeteoSwiss/publication-opendata/tree/master#212-smn-automatic-measurements)
        - nime (manual-measurements)
        - obs (manual-observations)
        - climate (climate)
            - records
        - pollen (pollen-monitoring)
        - phenology (phenological-observations)
        - ~~aerosol~~
    - atmosphere
        - radiosounding
        - remote sensing (was 'radar')
        - ...
    - model
        - postprocessed data (Data4Web)
        - nowcasting-inca
        - COSMO/ICON
        - ...
    - gridded data
        - climate data
        - radar and compiprecip

### 2.1. Surface ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/surface-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/surface-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/surface-IT))
MeteoSwiss operates a network of [land-based weather stations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations.html) where current weather and climate data are automatically recorded. It covers all parts of the country and all altitude levels. The measurements are supplemented with a wide array of additional observations, ranging from manual recording of cloud cover and vegetation development, to measurements of fine particulate matter, through to a network of cameras that covers all major sections of terrain and mountain passes in Switzerland.

#### 2.1.1. Open questions to the user community
1. [fill in Question 1](https://github.com/MeteoSwiss/publication-opendata/discussions/1)
2. [fill in Question 2](https://github.com/MeteoSwiss/publication-opendata/discussions/2)
3. ...

#### 2.1.2. smn (automatic-measurements)
SwissMetNet, the [automatic measurement network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html) of MeteoSwiss, comprises about 160 automatic stations with a full measurement program. These stations deliver a multitude of current data on weather and climate in Switzerland every ten minutes. The network is supplemented by automatic precipitation stations (about 100 stations). Together, these stations form the basis for the creation of reliable local weather forecasts as well as severe weather and flood warnings.

#### 2.1.2.1. Data

>*Open Data Product (Title):* **10-Minuten-SMN-Werte-...** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/smn-10min-now.csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/smn-10min-now.csv) <br>
>*Granularity:* ... <br>
>*Update frequency:* ... <br>
>*Format:* csv <br>
>*Volume (MB/GB/TB):* ... <br>
>*Additional remarks*: ... <br>

#### 2.1.2.2. Metadata

| Field Name          | Description                                | Format     | Note |
|---------------------|--------------------------------------------|------------|------|
| __date__              | Date of notification                       | YYYY-MM-DD | |
| __time__                 | Time of notification                       | HH:MM      | |
| __abbreviation_canton_and_fl__  | Abbreviation of the reporting canton       | Text       | |
| __ncumul_tested__      | Reported number of tests performed as of date| Number     | Irrespective of canton of residence |

<!-- Metadaten als .csv -->
