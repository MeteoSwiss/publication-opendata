# OGD@MeteoSwiss - Open Government Data

<!-- Tabelle mit 4 sprachen in spalten, statt Übersetzungen in Files? -->

- 2.2. [surface](https://github.com/MeteoSwiss/publication-opendata/tree/master#21-surface-de-fr-it)
  - 2.2.1. [automatic-measurements (smn, smn-precip, smn-tower)](https://github.com/MeteoSwiss/publication-opendata#221-automatic-weather-stations-smn-smn-precip-smn-tower)
  - 2.2.x. ~~aviation~~
  - 2.2.2. [manual-precipitation-measurements (nime, tot)](https://github.com/MeteoSwiss/publication-opendata#222-manual-precipitation-stations-nime-tot)
  - 2.2.3. [visual-observations (obs)](https://github.com/MeteoSwiss/publication-opendata#223-visual-observations-obs)
  - 2.2.4. [point-climate (climate, climate-precip)](https://github.com/MeteoSwiss/publication-opendata#224-climate-stations-swiss-nbcn-climate-climate-precip) and records
  - 2.2.5. [pollen-monitoring (pollen)](https://github.com/MeteoSwiss/publication-opendata#224-swiss-pollen-monitoring-stations-pollen)
  - 2.2.6. [phenological-observations (phenology)](https://github.com/MeteoSwiss/publication-opendata#225-phenological-observations-phenology)
  - 2.2.x. ~~aerosol~~
- 2.3. [atmosphere](https://github.com/MeteoSwiss/publication-opendata/tree/main#22-atmosphere-de-fr-it)
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
- 2.4. [model data](https://github.com/MeteoSwiss/publication-opendata/tree/main#24-model-data).
  - postprocessed data (Data4Web) (?)
  - [INCA (nowcasting)](https://github.com/MeteoSwiss/publication-opendata/tree/main#242-INCA-data).
  - COSMO/ICON
  - ...
- 2.5. grid
  - climate data (spatial data)
  - radar and compiprecip
 
    
## 1. Context and mission ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/context-and-purpose-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/context-and-purpose-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/context-and-purpose-IT))
In order to legally implement the [Federal Act on the use of electronic means for the performance of official duties' (EMBAG)](https://www.meteoswiss.admin.ch/about-us/remit-and-legal-mandate.html) the overall revision of the Ordinance on Meteorology and Climatology (MetV; SR 429.11) is now pending. In the current year (2023) the necessary technical and organizational measures for the implementation of OGD at MeteoSwiss are being tackled within the scope of a project.

### 1.1. Purpose of this repository
This repository is used by MeteoSwiss to inform potential users interested in open data about the plans and to receive specific feedback from them on proposals. **We describe below the open data products being designed by the various interdisciplinary data teams.** That is: the **data structures, formats, denominations, update frequencies, volumes and other specifics.**

All information reflects the current state of work and is subject to change. Finding out, collecting, analysing and weighting user needs is the central way for MeteoSwiss to be able to offer good open data products.

Thank you very much for your attention and openness to enter into an exchange with us for this purpose.

### 1.2. General contact point
If you have any questions, please contact the project core team: [opendata(at)meteoswiss.ch](mailto:opendata@meteoswiss.ch)

## 2. Open data products ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/opendata-products-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/opendata-products-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/opendata-products-IT))

### 2.1. General information
MeteoSwiss operates an extensive monitoring network, both on the ground (surface stations) and in the atmosphere, that enables it to collect round-the-clock meteorological data for the whole of Switzerland. These data form the basis for making weather forecasts, issuing bad weather warnings, and analysing climate change. Furthermore MeteoSwiss operates a weather model for forecasting and also generates gridded data sets. All these different data types are described below and are available under an open data license.

#### 2.1.1. Granulartiy of MeteoSwiss data
For all types of data MeteoSwiss uses standard granularities. Depending on the application not all granularites are available. For measurement data the lowest granulartiy is usually called raw data (Rohwert) or orignal data (Originalwert) and higher granularties are called aggregations or aggregated values. The world meteorological organization (WMO) does issue guidelines on how national weather services have to aggregate values and MeteoSwiss does follow these guidelines. So if you need hourly, daily, monthly or yearly values, we strongly recommend that you download the according granularity. Downloading the raw data (10min) and calculating sums or means yourself, will not always lead to the same results! Furthermore for historic data it is possibly that manual data corrections have only been applied on higher granularities (like hourly or daily data), which means that historic raw data can still contain errors. Here is an overview of the granularities used in MeteoSwiss:

| Granularity | Name | Description | Examples |
| --- | --- | --- | --- |
| T | 10min value | At MeteoSwiss this is the standard granularity for realtime data of the automatic measurement network SwissMetNet or the model output. Meteorological observations do also use this granularity but only offer values at fixed intervals like 6UTC, 12UTC and 18UTC (called "Terminwerte")! | [SMN](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html), [OBS](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-observation-network.html) |
| H | Hourly value | Either aggregated from 10min values or provided by the instrument/network | [Pollen](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) |
| D | Daily value | Used throught the MeteoSwiss measurement network before automatization in 1981 started. Today still used for manual precipitation and snow measurements. For automatic stations daily values are calculated using 10 min values according to WMO guidelines. | [NIME](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html) |
| M | Monthly value | Usually aggregated from daily values and widely used in climatology for homogenized data and norm values and for seasonal data. For some very old data series (pre 1864) only monthly data exists!| [Homogeneous data series](https://www.meteoswiss.admin.ch/climate/climate-change/changes-in-temperature-precipitation-and-sunshine/homogeneous-data-series-since-1864.html), [Climate normals](https://www.meteoswiss.admin.ch/climate/the-climate-of-switzerland/climate-normals.html) |
| Y | Yearly value | Usually aggregated from daily values and mostly used in climatology or climage change screnarios. | [Climate change scenarios](https://www.meteoswiss.admin.ch/climate/climate-change/swiss-climate-change-scenarios.html)|

#### 2.1.2. Structure and update cycle
For measurement data MeteoSwiss provides an optimized directory structure separating older historical data, which is not updated regularly and more recent data, which is updated more often. For realtime data we provide a third "now" directory with a high update frequency. Here is the overview:

| Type | Description | Update cycle | Used for |
| --- | --- | --- | --- |
| historical | From the start of the measurement until the 31st of december of last year | Once a year  | Granularity M, D, H, T |
| recent | From January 1st of this year until yesterday | Daily at 12UTC | Granularity M, D, H, T |
| now | The most recent realtime data from yesterday 12UTC to now | Every 10min | Only Granularity H, T |
| `no type` | For certain data types this concept does not apply | varies | varies (e.g. Granularity Y) |

#### 2.1.3. Time stamps and time intervals
All reference time stamps at MeteoSwiss are in UTC! Depending on the granularity the time stamp does define different intervals:
- T: The sum, mean or max/min of the last 10 minutes (ReferenceTS 16:00 = `15:50:01 to 16:00:00`)
- H: The sum, mean or max/min of the last six 10min-values (ReferenceTS 16:00 = `15:10 to 16:00`). Please note: Hourly values before 2018 were calculated differently based on the SYNOP schedule (ReferenceTS 16:00 = `14:50 to 15:40`)! 
- D: For most parameters the sum, mean or max/min from 00:00 to 23:50 of the according date. Exception for precipitation and snow (manual measurement times used for consistency) where the interval is 6:00 UTC until 5:50 UTC tomorrow (ReferenceTS 22.6.2023 = `22.6.2023 6:10 UTC to 23.6.2023 6:00 UTC`)
- M: The sum, mean or max/min of the whole month from 1st to last day of month (ReferenceTS 1.6.2023 = `1.6.2023 00:10 UTC to 30.6.2023 24:00 UTC`)
- Y: The sum, mean or max/min of the whole year (ReferenceTS 1.1.2023 = `1.1.2023 00:10 UTC to 31.12.2023 24:00 UTC`)

So for granularity T and H the time stamp defines the end of the measurement interval and for higher granularities (D, M and Y) the time stamp defines the beginning of the interval!

#### 2.1.4. General questions to the open data user community 
1. [Besides wind guts (maximum wind speed) MeteoSwiss plans to only publish maximum and minimum (hourly, daily, monthly and yearly) for temperature, since these aggregations are widely used and used to be measured by separate instruments in the past. Du users want to have aggregated (calculate) maximum and minimum also for other parameters like pressure, humidity or soil parameters or will they calculate these themselves?](https://github.com/MeteoSwiss/publication-opendata/discussions/1)
2. [For sum parameters (precipitation, snow) MeteoSwiss plans to only publish one parameter per granularity. Do users want to have multi-hour (e.g. 6h, 12h, 24h) or multi-day (2d, 3d, 6d) aggregated sums or will they calculate these themselves?](https://github.com/MeteoSwiss/publication-opendata/discussions/2)
3. Is the mutation information (e.g. if a value is original, interpolated, automatically or manually corrected, aggregated etc.) or a value interesting for the user? If yes, in which format should we publish this data?
4. What kind of metadata for stations and parameters does the user community expect from MeteoSwiss? Are the examples below sufficient or does the OGD community need more metadata?


### 2.2. Surface ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/surface-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/surface-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/surface-IT))
MeteoSwiss operates a network of [land-based weather stations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations.html) where current weather and climate data are automatically recorded. It covers all parts of the country and all altitude levels. The measurements are supplemented with a wide array of additional observations, ranging from manual recording of cloud cover and vegetation development, to measurements of fine particulate matter, through to a network of cameras that covers all major sections of terrain and mountain passes in Switzerland.

All MeteoSwiss surface stations have a name and an identfier consiting of three letters (e. g. BER for Bern / Zollikofen or LUG for Lugano). Data files use this station identifier in the file name throughout the all directories. A list of all station identfiers with station names, coordinates, height etc. can be found in the according metadata section.

#### 2.2.1. Automatic weather stations (smn, smn-precip, smn-tower)
SwissMetNet, the [automatic measurement network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html) of MeteoSwiss, comprises about 160 automatic stations with a full measurement program (type "smn"). These stations deliver a multitude of current data on weather and climate in Switzerland every ten minutes. The network is supplemented by around 100 automatic precipitation stations (type "smn-precip"). Together, these stations form the basis for the creation of reliable local weather forecasts as well as severe weather and flood warnings. Additionally MeteoSwiss operates three tower stations at 150m to 230m above ground for boundry layer measurements (type "smn-tower").

>*Open Data Product (Title):* **Measurement data from automatic weather stations** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/smn/10min/recent/smn_T_recent_SMA.csv](https://github.com/MeteoSwiss/publication-opendata/smn/10min/recent/smn_T_recent_SMA.csv) <br>
>*Granularity:* T, H, D, M and Y (see [chapter 2.1.1](#211-granulartiy-of-meteoswiss-data) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2](#212-structure-and-update-cycle) for more details! <br>
>*Format:* csv <br>
>*Network map:* [SwissMetNet](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>

#### 2.2.2. Manual precipitation stations (nime, tot)
In addition to its automatic precipitation measurements, MeteoSwiss also operates a [manual precipitation monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html). Measurements are taken here once a day and transmitted to MeteoSwiss via SMS. The network comprises 243 locations, 190 stations measure rainfall and snowfall and 53 stations measure snowfall only (nime). Due to their long-series measurements, they are of great climatological significance. In mountainous areas that are difficult to access, around 57 totalisers are used which record the volume of precipitation for an entire year (tot).

>*Open Data Product (Title):* **Measurement data from manual precipitation stations** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/nime/daily/historical/nime_D_historical_PFA.csv](https://github.com/MeteoSwiss/publication-opendata/nime/daily/historical/nime_D_historical_PFA.csv) <br>
>*Granularity:* D, M and Y (see [chapter 2.1.1](#211-granulartiy-of-meteoswiss-data) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2](#212-structure-and-update-cycle) for more details! <br>
>*Format:* csv <br>
>*Network map:* [NIME and TOT](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-manuell&lang=en&table=false) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-manuell/ch.meteoschweiz.messnetz-manuell_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>

#### 2.2.3. Visual observations (obs)
The information on current weather events is supplemented by [visual human observations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-observation-network.html). The atmospheric conditions around the observation site are described in detail.

>*Open Data Product (Title):* **Measurement data from visual observations** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/obs/hourly/recent/obs_H_recent_TAV.csv](https://github.com/MeteoSwiss/publication-opendata/publication-opendata/obs/hourly/recent/obs_H_recent_TAV.csv) <br>
>*Granularity:* T (see [chapter 2.1.1](#211-granulartiy-of-meteoswiss-data) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2](#212-structure-and-update-cycle) for more details! <br>
>*Format:* csv <br>
>*Network map:* [OBS](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-beobachtungen&lang=en&table=false) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-beobachtungen/ch.meteoschweiz.messnetz-beobachtungen_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>

#### 2.2.4. Climate stations "Swiss NBCN" (climate, climate-precip)
The [Swiss National Basic Climatological Network "Swiss NBCN"](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/swiss-national-basic-climatological-network.html) connects the major ground-based stations within the MeteoSwiss monitoring network. It consists of 29 climate monitoring stations and 46 precipitation stations. The measurement series available in digital form for temperature, precipitation and hours of sunshine date back, in some cases, to the mid-nineteenth century.

>*Open Data Product (Title):* **Measurement data from the Swiss National Basic Climatological Network** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/climate/monthly/historical/climate_M_historical_GSB.csv](https://github.com/MeteoSwiss/publication-opendata/climate/monthly/historical/climate_M_historical_GSB.csv) <br>
>*Granularity:* D, M and Y (see [chapter 2.1.1](#211-granulartiy-of-meteoswiss-data) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2](#212-structure-and-update-cycle) for more details! <br>
>*Format:* csv <br>
>*Network map:* [CLIMATE](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-klima&lang=en&table=false) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-klima/ch.meteoschweiz.messnetz-klima_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>

Additionally the top 10 records of every climate station and the overall records can be downloaded per parameter separately. TBD...

#### 2.2.4. Swiss pollen monitoring stations (pollen)
MeteoSwiss operates the [national pollen monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/pollen-monitoring-network-manual-method.html). This consists of 14 monitoring stations which cover Switzerland's most important climatic and vegetation regions. The measurements obtained provide invaluable information for those who suffer from allergies. Additionally since 2023 the new [automatic pollen network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) is now operational: for the first time in the world, instead of daily averages being available after a week, information is available in real time at an hourly resolution.

>*Open Data Product (Title):* **Measurement data from the Swiss pollen monitoring network** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/pollen/hourly/recent/pollen_H_recent_PBS.csv](https://github.com/MeteoSwiss/publication-opendata/pollen/hourly/recent/pollen_H_recent_PBS.csv) <br>
>*Granularity:* H, D, M and Y (see [chapter 2.1.1](#211-granulartiy-of-meteoswiss-data) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2](#212-structure-and-update-cycle) for more details! <br>
>*Format:* csv <br>
>*Network map:* [Pollen](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-pollen&lang=en&table=false) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-pollen/ch.meteoschweiz.messnetz-pollen_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>

#### 2.2.5. Phenological observations (phenology)
The [Swiss Phenology Network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/swiss-phenology-network.html) consists of 160 stations. Some 26 different plant species are observed in order to describe the vegetation development. On the basis of this information, it is possible to investigate the impact of climate change on the vegetation. The observations also serve to generate forecasting models for the start of flowering.

>*Open Data Product (Title):* **Measurement data from the Swiss phenology network** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/phenology/yearly/historical/phenology_Y_historical_ADB.csv](https://github.com/MeteoSwiss/publication-opendata/phenology/yearly/historical/phenology_Y_historical_ADB.csv) <br>
>*Granularity:* Y (see [chapter 2.1.1](#211-granulartiy-of-meteoswiss-data) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2](#212-structure-and-update-cycle) for more details! <br>
>*Format:* csv <br>
>*Network map:* [Phenology](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-phaenologie&lang=en&table=false) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-phaenologie/ch.meteoschweiz.messnetz-phaenologie_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>


### 2.3. Atmosphere ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/atmosphere-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/atmosphere-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/atmosphere-IT))
...

#### 2.3.1. Open questions to the user community about data in the 'atmosphere' category
1. [fill in Question X](https://github.com/MeteoSwiss/publication-opendata/discussions/X)
2. [fill in Question Y](https://github.com/MeteoSwiss/publication-opendata/discussions/Y)
3. ...

#### 2.3.2. ...
...

#### 2.3.2.1. Discovery metadata w/ data structure

>*Open Data Product (Title):* **...** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv) <br>
>*Granularity:* ... <br>
>*Update frequency:* ... <br>
>*Format:* ... <br>
>*Volume (MB/GB/TB):* ... <br>
>*Additional remarks*: ... <br>

#### 2.3.2.2. File-level metadata

| Field Name          | Description                                | Format     | Note |
|---------------------|--------------------------------------------|------------|------|
| __date__              | Date of notification                       | YYYY-MM-DD | |
| __time__                 | Time of notification                       | HH:MM      | |
| __abbreviation_canton_and_fl__  | Abbreviation of the reporting canton       | Text       | |
| __ncumul_tested__      | Reported number of tests performed as of date| Number     | Irrespective of canton of residence |



#### 2.4. Model data

#### 2.4.1. postprocessed data





#### 2.4.2. INCA data

>*Open Data Product (Title):* **INCA Precipitation quantitative (RR)** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 1.8 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 <br>

>*Open Data Product (Title):* **INCA Precipitation quantitative extended forecast (RR_ext)** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 20 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

<!-- Metadaten als .csv -->
