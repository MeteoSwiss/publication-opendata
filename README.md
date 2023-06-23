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

### 1.3. Granulartiy of MeteoSwiss data
For all types of data MeteoSwiss uses standard granularities. Depending on the application not all granularites are available. For measurement data the lowest granulartiy is usually called raw data (Rohwert) or orignal data (Originalwert) and higher granularties are called aggregations or aggregated values. The world meteorological organization (WMO) does issue guidelines on how national weather services have to aggregate values and MeteoSwiss does follow these guidelines. So if you need hourly, daily, monthly or yearly values, we strongly recommend that you download the according granularity. Downloading the raw data (10min) and calculating sums or means yourself, will not always lead to the same results! Furthermore for historic data it is possibly that manual data corrections have only been applied on higher granularities (like hourly or daily data), which means that historic raw data can still contain errors. Here is an overview of the granularities used in MeteoSwiss:

| Granularity | Name | Description | Examples |
| --- | --- | --- | --- |
| I | Instant value (<10min) | Everything below 10 min, not used very often at MeteoSwiss.  | [Radar](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/weather-radar-network.html), [SACRaM](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/radiation-monitoring-network.html) |
| T | 10min value | At MeteoSwiss this is usually the lowest standard granularity of the automatic measurement network SwissMetNet or model output. Meteorological observations do also use this granularity but only offer values at fixed intervals like 6UTC, 12UTC and 18UTC (called "Terminwerte")! | [SMN](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html), [OBS](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-observation-network.html) |
| H | Hourly value | Either aggregated from 10min values or provided by the instrument/network | [Pollen](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) |
| D | Daily value | Used throught the MeteoSwiss measurement network before automatization in 1981 started. Today still used for manual precipitation and snow measurements. For automatic stations daily values are calculated using 10 min values according to WMO guidelines. | [NIME](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html) |
| M | Monthly value | Usually aggregated from daily values and widely used in climatology for homogenized data and norm values and for seasonal data. For some very old data series (pre 1864) only monthly data exists!| [Homogeneous data series](https://www.meteoswiss.admin.ch/climate/climate-change/changes-in-temperature-precipitation-and-sunshine/homogeneous-data-series-since-1864.html), [Climate normals](https://www.meteoswiss.admin.ch/climate/the-climate-of-switzerland/climate-normals.html) |
| Y | Yearly value | Usually aggregated from daily values and mostly used in climatology or climage change screnarios. | [Climate change scenarios](https://www.meteoswiss.admin.ch/climate/climate-change/swiss-climate-change-scenarios.html)|

<!-- Tabelle mit 4 sprachen in spalten, statt Übersetzungen in Files? -->

- 2.1. [surface](https://github.com/MeteoSwiss/publication-opendata/tree/master#21-surface-de-fr-it)
  - 2.1.1. [automatic-measurements (smn)](https://github.com/MeteoSwiss/publication-opendata/tree/master#212-smn-automatic-measurements)
  - 2.1.2. ~~aviation~~
  - 2.1.3. manual-precipitation-measurements (nime)
  - 2.1.4. manual-observations (obs)
  - 2.1.5. point-climate (climate)
    - records
  - 2.1.6. pollen-monitoring (pollen)
  - 2.1.7. phenological-observations (phenology)
  - 2.1.8. ~~aerosol~~
- 2.2. [atmosphere](https://github.com/MeteoSwiss/publication-opendata/tree/main#22-atmosphere-de-fr-it)
  - ((weather balloon)) radiosondes (radiosounding)
  - weather-radar (remotesensing)
  - (?) "Windprofiler"
  - (?) "LIDAR and ceilometers"
  - (?) "Microwave Radiometry"
  - ~~Observations from aircraft~~
  - ~~Satellite observations~~
  - (?) "Ozone measurements"
  - ~~"Lightning detection network"~~
  - (?) "Radiation monitoring network"
- 2.3. model
  - postprocessed data (Data4Web) (?)
  - ~~nowcasting~~inca (nowcasting) (?)
  - COSMO/ICON
  - ...
- 2.4. grid
  - climate data (spatial data)
  - radar and compiprecip

### 2.1. Surface ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/surface-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/surface-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/surface-IT))
MeteoSwiss operates a network of [land-based weather stations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations.html) where current weather and climate data are automatically recorded. It covers all parts of the country and all altitude levels. The measurements are supplemented with a wide array of additional observations, ranging from manual recording of cloud cover and vegetation development, to measurements of fine particulate matter, through to a network of cameras that covers all major sections of terrain and mountain passes in Switzerland.

#### 2.1.1. Open questions to the user community about data in the 'surface' category
1. [fill in Question 1](https://github.com/MeteoSwiss/publication-opendata/discussions/1)
2. [fill in Question 2](https://github.com/MeteoSwiss/publication-opendata/discussions/2)
3. ...

#### 2.1.2. Automatic weather stations (smn, smn-precip, smn-tower)
SwissMetNet, the [automatic measurement network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html) of MeteoSwiss, comprises about 160 automatic stations with a full measurement program (type "smn"). These stations deliver a multitude of current data on weather and climate in Switzerland every ten minutes. The network is supplemented by around 100 automatic precipitation stations (type "smn-precip"). Together, these stations form the basis for the creation of reliable local weather forecasts as well as severe weather and flood warnings. Additionally MeteoSwiss operates three tower stations at 150m to 230m above ground for boundry layer measurements (type "smn-tower").

#### 2.1.2.1. Discovery metadata w/ data structure

>*Open Data Product (Title):* **10-Minuten-SMN-Werte-...** <br>
>**Data structure (Example file):** [https://github.com/MeteoSwiss/publication-opendata/blob/main/smn-10min-now.csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/smn-10min-now.csv) <br>
>*Granularity:* ... <br>
>*Update frequency:* ... <br>
>*Format:* csv <br>
>*Volume (MB/GB/TB):* ... <br>
>*Additional remarks*: ... <br>

#### 2.1.2.2. File-level metadata

| Field Name          | Description                                | Format     | Note |
|---------------------|--------------------------------------------|------------|------|
| __date__              | Date of notification                       | YYYY-MM-DD | |
| __time__                 | Time of notification                       | HH:MM      | |
| __abbreviation_canton_and_fl__  | Abbreviation of the reporting canton       | Text       | |
| __ncumul_tested__      | Reported number of tests performed as of date| Number     | Irrespective of canton of residence |

<!-- Metadaten als .csv -->

#### 2.2.2. ...
...

#### 2.2.2.1. Discovery metadata w/ data structure

>*Open Data Product (Title):* **...** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv) <br>
>*Granularity:* ... <br>
>*Update frequency:* ... <br>
>*Format:* ... <br>
>*Volume (MB/GB/TB):* ... <br>
>*Additional remarks*: ... <br>

#### 2.1.2.2. File-level metadata

| Field Name          | Description                                | Format     | Note |
|---------------------|--------------------------------------------|------------|------|
| __date__            | Date of notification                       | YYYY-MM-DD |      |

### 2.2. Atmosphere ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/atmosphere-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/atmosphere-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/atmosphere-IT))
...

#### 2.2.1. Open questions to the user community about data in the 'atmosphere' category
1. [fill in Question X](https://github.com/MeteoSwiss/publication-opendata/discussions/X)
2. [fill in Question Y](https://github.com/MeteoSwiss/publication-opendata/discussions/Y)
3. ...

#### 2.2.2. ...
...

#### 2.2.2.1. Discovery metadata w/ data structure

>*Open Data Product (Title):* **...** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv) <br>
>*Granularity:* ... <br>
>*Update frequency:* ... <br>
>*Format:* ... <br>
>*Volume (MB/GB/TB):* ... <br>
>*Additional remarks*: ... <br>

#### 2.1.2.2. File-level metadata

| Field Name          | Description                                | Format     | Note |
|---------------------|--------------------------------------------|------------|------|
| __date__              | Date of notification                       | YYYY-MM-DD | |
| __time__                 | Time of notification                       | HH:MM      | |
| __abbreviation_canton_and_fl__  | Abbreviation of the reporting canton       | Text       | |
| __ncumul_tested__      | Reported number of tests performed as of date| Number     | Irrespective of canton of residence |

<!-- Metadaten als .csv -->
