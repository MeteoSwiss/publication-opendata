*Version, status:* v1.0, DRAFT <br>
*Maintainer:* Federal Office of Meteorology and Climatology MeteoSwiss, [OGD@MeteoSwiss Project Team](mailto:opendata@meteoswiss.ch)

[![GitHub commit](https://img.shields.io/github/last-commit/MeteoSwiss/publication-opendata)](https://github.com/MeteoSwiss/publication-opendata/commits/master)

# OGD@MeteoSwiss - Open Government Data

> **This is work in progress.** <br>
> Jump directly to the overview of [which data types are to be made available as Open Data](https://github.com/MeteoSwiss/publication-opendata/tree/master#21-general-information-and-status-of-clarifications).


## Table of contents

1. [Context and mission of the project](https://github.com/MeteoSwiss/publication-opendata/tree/master#1-context-and-mission-of-this-project)
    - 1.1. [Purpose of this repository](https://github.com/MeteoSwiss/publication-opendata/tree/master#11-purpose-of-this-repository)
    - 1.2. [General contact point](https://github.com/MeteoSwiss/publication-opendata/tree/master#12-general-contact-point)
2. [Open data products](https://github.com/MeteoSwiss/publication-opendata/tree/master#2-open-data-products)
    - 2.1. [General information and status of clarifications](https://github.com/MeteoSwiss/publication-opendata/tree/master#21-general-information-and-status-of-clarifications)
        - 2.1.1. [Data granularity](https://github.com/MeteoSwiss/publication-opendata/tree/master#211-data-granularity)
        - 2.1.2. [Data structure and update cycle](https://github.com/MeteoSwiss/publication-opendata/tree/master#212-data-structure-and-update-cycle)
        - 2.1.3. [Time stamps and time intervals](https://github.com/MeteoSwiss/publication-opendata/tree/main#213-time-stamps-and-time-intervals)
        - 2.1.4. [Column separators, decimal dividers and missing values](https://github.com/MeteoSwiss/publication-opendata/tree/main#214-column-separators-decimal-dividers-and-missing-values)
    - 2.2. [Surface data](https://github.com/MeteoSwiss/publication-opendata/tree/master#22-surface-data)
        - 2.2.1. [Automatic weather stations (smn, smn-precip, smn-tower)](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-automatic-weather-stations-smn-smn-precip-smn-tower)
        - 2.2.2. [Manual precipitation stations (nime, tot)](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-manual-precipitation-stations-nime-tot)
        - 2.2.3. [Visual observations (obs)](https://github.com/MeteoSwiss/publication-opendata/tree/main#223-visual-observations-obs)
        - 2.2.4. [Climate stations "Swiss NBCN" (climate, climate-precip)](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-climate-stations-swiss-nbcn-climate-climate-precip)
        - 2.2.5. [Swiss pollen monitoring stations (pollen)](https://github.com/MeteoSwiss/publication-opendata/tree/main#225-swiss-pollen-monitoring-stations-pollen)
        - 2.2.6. [Phenological observations (phenology)](https://github.com/MeteoSwiss/publication-opendata/tree/main#226-phenological-observations-phenology)
    - 2.3. [Atmosphere data](https://github.com/MeteoSwiss/publication-opendata/tree/main#23-atmosphere-data)
        - 2.3.1. [Radio soundings (radiosounding)](https://github.com/MeteoSwiss/publication-opendata/tree/main#231-radio-soundings-radiosounding)
        - 2.3.2. [Weather radar network (remotesensing)](https://github.com/MeteoSwiss/publication-opendata/tree/main#232-weather-radar-network-remotesensing)
    - 2.4. [Model data](https://github.com/MeteoSwiss/publication-opendata/tree/main#24-model-data)
        - 2.4.1. [INCA data (nowcasting)](https://github.com/MeteoSwiss/publication-opendata/tree/main#241-inca-data-nowcasting)
        - 2.4.2. COSMO/ICON data (forecasting)
    - 2.5. [Grid data](https://github.com/MeteoSwiss/publication-opendata/tree/main#25-grid-data)
        - 2.5.1. [Spatial climate data](https://github.com/MeteoSwiss/publication-opendata/tree/main#251-Spatial-climate-data)
        - 2.5.2. [Radar and combiprecip data](https://github.com/MeteoSwiss/publication-opendata/tree/main#252-Radar-and-combiprecip-data)
3. [Questions to the open data user community](https://github.com/MeteoSwiss/publication-opendata/blob/main/README.md#3-questions-to-the-open-data-user-community)
 
    
## 1. Context and mission of this project
In order to legally implement the [Federal Act on the use of electronic means for the performance of official duties' (EMBAG)](https://www.meteoswiss.admin.ch/about-us/remit-and-legal-mandate.html) the overall revision of the Ordinance on Meteorology and Climatology (MetV; SR 429.11) is now pending.

In the current year (2023) the necessary technical and organizational measures for the implementation of Open Government Data (OGD) at [MeteoSwiss](https://www.meteoswiss.admin.ch/about-us/portrait.html) are being tackled within the scope of a project.

> **Finding out, collecting, analysing and weighting user needs** is the central way for the project team to be able to offer good 'open data products'.
> Thank you very much for your attention and your openness to enter into an exchange with us on this matter.

### 1.1. Purpose of this repository
This repository is used by MeteoSwiss' project team to inform potential users interested in open data about the plans and to receive specific feedback from them on proposals.
1. [We describe the various 'open data products'](https://github.com/MeteoSwiss/publication-opendata/tree/main#2-open-data-products) being designed by MeteoSwiss' specialist data teams. That is: the **data structures, formats, denominations, update frequencies, volumes and other specifics**.
2. We are looking for your feedback on our proposals: To this end, [we ask you general questions](https://github.com/MeteoSwiss/publication-opendata/tree/main#3-questions-to-the-open-data-user-community) on the one hand, and are open to your specific questions and feedback on the other. <br>
> **The preferred way to share the latter is to [open a public issue in this repository](https://github.com/MeteoSwiss/publication-opendata/issues/new).**
> Alternatively, [write us an email](https://github.com/MeteoSwiss/publication-opendata/tree/main#12-general-contact-point).
> **The data teams meet every second week** to review and clarify the feedback received, to provide answers or ask questions if necessary.

**Important note:**
- All information in this repository reflects the current state of work and is subject to change.

### 1.2. General contact point
If you have any questions, please contact the project team: [opendata(at)meteoswiss.ch](mailto:opendata@meteoswiss.ch)

## 2. Open data products

### 2.1. General information and status of clarifications
MeteoSwiss operates an extensive monitoring network, both on the ground (surface stations) and in the atmosphere, that enables it to collect round-the-clock meteorological data for the whole of Switzerland. These data form the basis for making weather forecasts, issuing bad weather warnings, and analysing climate change. Furthermore MeteoSwiss operates a weather model for forecasting and also generates gridded data sets.

This is the **current status of the clarifications** as to which data types can be made available (and how) under an open data license by MeteoSwiss, and which not:

| Data category | in clarification if/what | can be made available as open data | cannot be made available as open data - with reasons | 
| :------------ | :----------------------- | :--------------------------------- | :--------------------------------------------------- |
| **Surface** | [Aerosol measurements](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/aerosol-measurements.html) | [Automatic weather stations](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-automatic-weather-stations-smn-smn-precip-smn-tower) | [Aviation weather](https://www.meteoswiss.admin.ch/services-and-publications/service/weather-and-climate-products/aviation-weather.html) - These data are collected on behalf of and financed by professional aviation |
|  |  | [Manual precipitation stations](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-manual-precipitation-stations-nime-tot) |  |
|  |  | [Visual observations](https://github.com/MeteoSwiss/publication-opendata/tree/main#223-visual-observations-obs) |  |
|  |  | [Climate stations "Swiss NBCN"](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-climate-stations-swiss-nbcn-climate-climate-precip) |  |
|  |  | [Swiss pollen monitoring stations](https://github.com/MeteoSwiss/publication-opendata/tree/main#225-swiss-pollen-monitoring-stations-pollen) |  |
|  |  | [Phenological observations](https://github.com/MeteoSwiss/publication-opendata/tree/main#226-phenological-observations-phenology) |  |
| **Atmosphere** | [Windprofiler](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/windprofiler.html) | [Radio soundings](https://github.com/MeteoSwiss/publication-opendata/tree/main#231-radio-soundings-radiosounding) | [Observations from aircraft](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/observations-from-aircraft.html) - Data does not belong to MeteoSwiss |
|  | [LIDAR and ceilometers](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/lidar-and-ceilometers.html) | [Weather radar network](https://github.com/MeteoSwiss/publication-opendata/tree/main#232-weather-radar-network-remotesensing) | [Satellite observations](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/satellite-observations.html) - Data does not belong to MeteoSwiss |
|  | [Microwave radiometry](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/microwave-radiometry.html) |  | [Lightning detection network](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/lightning-detection-network.html) - Data does not belong to MeteoSwiss |
|  | [Ozone measurements](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/ozone-measurements.html) |  |  |
|  | [Radiation monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/radiation-monitoring-network.html) |  |  |
| **Model** | Postprocessed data (Data4Web) | [Nowcasting data (INCA)](https://github.com/MeteoSwiss/publication-opendata/tree/main#241-inca-data-nowcasting) |  |
|  |  | Forecasting data (COSMO/ICON) |  |
| **Grid** |  | [Spatial climate data](https://github.com/MeteoSwiss/publication-opendata/tree/main#251-Spatial-climate-data) |  |
|  |  | [Radar and compiprecip data](https://github.com/MeteoSwiss/publication-opendata/tree/main#252-Radar-and-combiprecip-data) |  |


#### 2.1.1. Data granularity
For all types of data MeteoSwiss uses standard granularities. Depending on the application not all granularites are available. For measurement data the lowest granulartiy is usually called 'raw data' (Rohwert) or 'original data' (Originalwert). Higher granularities are called 'aggregations' or 'aggregated values'. The world meteorological organization (WMO) does issue guidelines on how national weather services have to aggregate values and MeteoSwiss does follow these guidelines.

If you need hourly, daily, monthly or yearly values, we strongly recommend that you download the according granularity. Downloading the raw data (10min) and calculating sums or means yourself, will not always lead to the same results! Furthermore for historic data it is possibly that manual data corrections have only been applied on higher granularities (like hourly or daily data), which means that historic raw data can still contain errors.

This is the overview of the granularities used by MeteoSwiss:

| Granularity | Name | Description | Used for |
| ----------- | ---- | ----------- | -------- |
| T | 10min value | At MeteoSwiss this is the standard granularity for realtime data of the automatic measurement network SwissMetNet (SMN) or the model output. Meteorological observations do also use this granularity but only offer values at fixed intervals like 6UTC, 12UTC and 18UTC (called "Terminwerte")! | [SMN](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html), [OBS](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-observation-network.html) |
| H | Hourly value | Either aggregated from 10min values or provided by the instrument/network | [Pollen](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) |
| D | Daily value | Used throughout the MeteoSwiss measurement network before automatization in 1981 started. Today still used for manual precipitation and snow measurements. For automatic stations daily values are calculated using 10min values according to WMO guidelines. | [NIME](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html) |
| M | Monthly value | Usually aggregated from daily values and widely used in climatology for homogenized data and norm values and for seasonal data. For some very old data series (pre 1864) only monthly data exists!| [Homogeneous data series](https://www.meteoswiss.admin.ch/climate/climate-change/changes-in-temperature-precipitation-and-sunshine/homogeneous-data-series-since-1864.html), [Climate normals](https://www.meteoswiss.admin.ch/climate/the-climate-of-switzerland/climate-normals.html) |
| Y | Yearly value | Usually aggregated from daily values and mostly used in climatology or climate change screnarios. | [Climate change scenarios](https://www.meteoswiss.admin.ch/climate/climate-change/swiss-climate-change-scenarios.html)|

#### 2.1.2. Data structure and update cycle
For measurement data MeteoSwiss provides an optimized directory structure separating older historical data, which is not updated regularly, and more recent data, which is updated more often. For realtime data we provide a third "now" directory with a high update frequency.

This is the overview:

| Type | Description | Update cycle | Used for |
| ---- | ----------- | ------------ | -------- |
| historical | From the start of the measurement until December 31st of last year | Once a year | [Granularity](https://github.com/MeteoSwiss/publication-opendata/tree/main#211-data-granularity) M, D, H, T |
| recent | From January 1st of this year until yesterday | Daily at 12UTC | [Granularity](https://github.com/MeteoSwiss/publication-opendata/tree/main#211-data-granularity) M, D, H, T |
| now | The most recent realtime data from yesterday 12UTC to now | Every 10min | Only [Granularity](https://github.com/MeteoSwiss/publication-opendata/tree/main#211-data-granularity) H, T |
| `no type` | For certain data types this concept does not apply | varies | varies (e.g. [Granularity](https://github.com/MeteoSwiss/publication-opendata/tree/main#211-data-granularity) Y) |

#### 2.1.3. Time stamps and time intervals
All reference time stamps at MeteoSwiss are in [UTC](https://www.utctime.net)! Depending on the granularity the time stamp does define different intervals:
- T: The sum, mean or max/min of the last 10 minutes (ReferenceTS 16:00 = `15:50:01 to 16:00:00`)
- H: The sum, mean or max/min of the last six 10min-values (ReferenceTS 16:00 = `15:10 to 16:00`). Please note: Hourly values before 2018 were calculated differently based on the SYNOP schedule (ReferenceTS 16:00 = `14:50 to 15:40`)! 
- D: For most parameters the sum, mean or max/min from 00:00 to 23:50 of the according date. Exception for precipitation and snow (manual measurement times used for consistency) where the interval is 6:00 UTC until 5:50 UTC tomorrow (ReferenceTS 22.6.2023 = `22.6.2023 6:10 UTC to 23.6.2023 6:00 UTC`)
- M: The sum, mean or max/min of the whole month from 1st to last day of month (ReferenceTS 1.6.2023 = `1.6.2023 00:10 UTC to 30.6.2023 24:00 UTC`)
- Y: The sum, mean or max/min of the whole year (ReferenceTS 1.1.2023 = `1.1.2023 00:10 UTC to 31.12.2023 24:00 UTC`)

**Accordingly, it follows that:**
- for granularity T and H the time stamp defines the end of the measurement interval and
- for higher granularities (D, M and Y) the time stamp defines the beginning of the interval!

#### 2.1.4. Column separators, decimal dividers and missing values
Generally, columns are separated with a semicolon (`;`). The decimal divider is a full stop (`.`). Missing values are indicated with a hyphen (`-`).

### 2.2. Surface data
MeteoSwiss operates a network of [land-based weather stations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations.html) where current weather and climate data are automatically recorded. It covers all parts of the country and all altitude levels. The measurements are supplemented with a wide array of additional observations, ranging from manual recording of cloud cover and vegetation development, to measurements of fine particulate matter, through to a network of cameras that covers all major sections of terrain and mountain passes in Switzerland.

All MeteoSwiss surface stations have a name and an identfier consisting of three letters (e.g. `BER` for [Bern / Zollikofen](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en&station=BER&chart=hour) or `LUG` for [Lugano](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en&station=LUG&chart=hour)). Data files use this station identifier in the file name throughout all directories. A list of all station identfiers with station names, coordinates, height etc. can be found in the according metadata section.

#### 2.2.1. Automatic weather stations (smn, smn-precip, smn-tower)
SwissMetNet, the [automatic measurement network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html) of MeteoSwiss, comprises about 160 automatic stations with a full measurement program (type "smn"). These stations deliver a multitude of current data on weather and climate in Switzerland every ten minutes. The network is supplemented by around 100 automatic precipitation stations (type "smn-precip"). Together, these stations form the basis for the creation of reliable local weather forecasts as well as severe weather and flood warnings. Additionally MeteoSwiss operates three tower stations at 150m to 230m above ground for boundry layer measurements (type "smn-tower").

>*Open Data Product (Title):* **Measurement data from automatic weather stations** <br>
>*Data structure (Example file):* [main/data-surface/...](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface) <br>
>*Granularity:* T, H, D, M and Y (see [chapter 2.1.1.](#211-data-of-meteoswiss-data-granularity) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2.](#212-data-structure-and-update-cycle) for more details <br>
>*Format:* CSV <br>
>*Volume (MB/GB/TB):* ... <br>
>*Network map:* [SwissMetNet](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>

#### 2.2.2. Manual precipitation stations (nime, tot)
In addition to its automatic precipitation measurements, MeteoSwiss also operates a [manual precipitation monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html). Measurements are taken here once a day and transmitted to MeteoSwiss via SMS. The network comprises 243 locations, 190 stations measure rainfall and snowfall and 53 stations measure snowfall only (nime). Due to their long-series measurements, they are of great climatological significance. In mountainous areas that are difficult to access, around 57 totalisers are used which record the volume of precipitation for an entire year (tot).

>*Open Data Product (Title):* **Measurement data from manual precipitation stations** <br>
>*Data structure (Example file):* [main/data-surface/...](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface) <br>
>*Granularity:* D, M and Y (see [chapter 2.1.1.](#211-data-of-meteoswiss-data-granularity) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2.](#212-data-structure-and-update-cycle) for more details <br>
>*Format:* CSV <br>
>*Volume (MB/GB/TB):* ... <br>
>*Network map:* [NIME and TOT](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-manuell&lang=en&table=false) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-manuell/ch.meteoschweiz.messnetz-manuell_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>

#### 2.2.3. Visual observations (obs)
The information on current weather events is supplemented by [visual human observations](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-observation-network.html). The atmospheric conditions around the observation site are described in detail.

>*Open Data Product (Title):* **Measurement data from visual observations** <br>
>*Data structure (Example file):* [main/data-surface/...](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface) <br>
>*Granularity:* T (see [chapter 2.1.1.](#211-data-of-meteoswiss-data-granularity) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2.](#212-data-structure-and-update-cycle) for more details <br>
>*Format:* CSV <br>
>*Volume (MB/GB/TB):* ... <br>
>*Network map:* [OBS](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-beobachtungen&lang=en&table=false) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-beobachtungen/ch.meteoschweiz.messnetz-beobachtungen_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>

#### 2.2.4. Climate stations "Swiss NBCN" (climate, climate-precip)
The [Swiss National Basic Climatological Network "Swiss NBCN"](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/swiss-national-basic-climatological-network.html) connects the major ground-based stations within the MeteoSwiss monitoring network. It consists of 29 climate monitoring stations and 46 precipitation stations. The measurement series available in digital form for temperature, precipitation and hours of sunshine date back, in some cases, to the mid-nineteenth century.

>*Open Data Product (Title):* **Measurement data from the Swiss National Basic Climatological Network** <br>
>*Data structure (Example file):* [main/data-surface/...](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface) <br>
>*Granularity:* D, M and Y (see [chapter 2.1.1.](#211-data-of-meteoswiss-data-granularity) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2.](#212-data-structure-and-update-cycle) for more details <br>
>*Format:* CSV <br>
>*Volume (MB/GB/TB):* ... <br>
>*Network map:* [CLIMATE](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-klima&lang=en&table=false) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-klima/ch.meteoschweiz.messnetz-klima_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>

<!-- ##### 2.2.4.1 Records and extremes
Additionally the top 10 records of every climate station and the overall records can be downloaded per parameter separately.

((TBD ..)) -->

#### 2.2.5. Swiss pollen monitoring stations (pollen)
MeteoSwiss operates the [national pollen monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/pollen-monitoring-network-manual-method.html). This consists of 14 monitoring stations which cover Switzerland's most important climatic and vegetation regions. The measurements obtained provide invaluable information for those who suffer from allergies. Additionally since 2023 the new [automatic pollen network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) is now operational: for the first time in the world, instead of daily averages being available after a week, information is available in real time at an hourly resolution.

>*Open Data Product (Title):* **Measurement data from the Swiss pollen monitoring network** <br>
>*Data structure (Example file):* [main/data-surface/...](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface) <br>
>*Granularity:* H, D, M and Y (see [chapter 2.1.1.](#211-data-of-meteoswiss-data-granularity) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") or hourly (directory "now") - see [chapter 2.1.2.](#212-data-structure-and-update-cycle) for more details <br>
>*Format:* CSV <br>
>*Volume (MB/GB/TB):* ... <br>
>*Network map:* [Pollen](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-pollen&lang=en&table=false) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-pollen/ch.meteoschweiz.messnetz-pollen_en.csv) <br>
>*Parameter metadata:* To be defined <br>
>*Additional remarks*: One file per station! <br>

#### 2.2.6. Phenological observations (phenology)
The [Swiss Phenology Network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/swiss-phenology-network.html) consists of 160 stations. Some 26 different plant species are observed in order to describe the vegetation development. On the basis of this information, it is possible to investigate the impact of climate change on the vegetation. The observations also serve to generate forecasting models for the start of flowering.

>*Open Data Product (Title):* **Measurement data from the Swiss phenology network** <br>
>*Data structure (Example files):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/phenology/phenology-historical](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/phenology/phenology-historical), [https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/phenology/phenology-recent](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/phenology/phenology-recent) <br>
>*Granularity:* Y (see [chapter 2.1.1.](#211-data-of-meteoswiss-data-granularity) for more details) <br>
>*Update frequency:* Yearly (directory "historical"), daily (directory "recent") - see [chapter 2.1.2.](#212-data-structure-and-update-cycle) for more details <br>
>*Format:* CSV <br>
>*Volume (MB):* 7.08 <br>
>*Network map:* [Phenology](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-phaenologie&lang=en&table=false) <br>
>*Station metadata:* [station list as CSV](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-phaenologie/ch.meteoschweiz.messnetz-phaenologie_en.csv) <br>
>*Parameter metadata:* [https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/phenology/phenology-metadata](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/phenology/phenology-metadata) <br>
>*Additional remarks*: One file for all stattions! <br>

### 2.3. Atmosphere data
MeteoSwiss obtains relevant data for weather forecasting and climate analysis from the [atmosphere](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere.html). The properties and composition of the atmosphere are studied using various instruments and methods, including weather balloons, satellites and laser equipment. Weather radar stations play an important role, as they record precipitation and thunderstorms throughout Switzerland in real time.

#### 2.3.1. Radio soundings (radiosounding)
MeteoSwiss performs soundings twice a day using weather balloon radiosondes. This allows important meteorology-related atmospheric values to be measured at high altitudes. The results of the latest [radio soundings](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/radio-soundings.html) are made available in the form of data files ([decoded data](https://www.meteoswiss.admin.ch/services-and-publications/applications/radio-soundings.html#tab=radio-soundings-decoded)) and graphs ([emagrams](https://www.meteoswiss.admin.ch/services-and-publications/applications/radio-soundings.html#tab=radio-soundings-emagram)).

The radiosondes measure air pressure, temperature and humidity. Attached to a [weather balloon](https://www.meteoswiss.admin.ch/weather/weather-and-climate-from-a-to-z/weather-balloon.html) and carried high into the atmosphere, the radiosonde also records the exact position, allowing altitude, wind speed and direction to be determined. The data obtained in this way are of great importance for weather forecasts and climate research. MeteoSwiss launches a weather balloon twice a day from the sounding station in Payerne. Special soundings are also carried out to determine other parameters such as ozone or aerosol concentrations. In addition, MeteoSwiss operators launch research flights, for which several radiosondes are attached to the same balloon. This allows the readings to be compared with each other, checked for quality and verified.

>*Open Data Product (Title):* **Atmosphere data from radio sounding station Payerne** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/atmosphere/radiosounding-PAY](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-atmosphere/radiosounding-PAY) <br>
>*Granularity:* ... (see [chapter 2.1.1.](#211-data-of-meteoswiss-data-granularity) for more details) <br>
>*Update frequency:* ... - see [chapter 2.1.2.](#212-structure-and-update-cycle) for more details! <br>
>*Format:* CSV <br>
>*Volume (MB/GB/TB):* ... <br>
>*Network map:* ... <br>
>*Station metadata:* ... <br>
>*Parameter metadata:* [https://github.com/MeteoSwiss/publication-opendata/blob/main/data-atmosphere/radiosounding-PAY-metadata](https://github.com/MeteoSwiss/publication-opendata/blob/main/atmosphere/radiosounding-PAY-metadata) <br>
>*Additional remarks*: ... <br>

#### 2.3.2. Weather radar network (remotesensing)
Supplementing the conventional precipitation measurements taken at ground level meteorological stations, MeteoSwiss operates a network of five weather radar stations which record every type of precipitation and storms in real time, are fully automated and, between them, cover the whole of Switzerland.

The sites are
- Albis near Zurich (equipped with the latest technology (dual polarisation) in 2012, monitors the atmosphere of the whole of northern Switzerland)
- Monte Lema in the Canton of Ticino (equipped with the latest technology (dual polarisation) in 2011, monitors the atmosphere of the whole of southern Switzerland)
- La Dôle near Geneva (equipped with the latest technology (dual polarisation) in 2011)
- Pointe de la Plaine Morte in the Canton of Valais (equipped with the latest technology (dual polarisation), commenced operation in 2014 and monitors the atmosphere in the inner Alpine region)
- the Weissfluhgipfel in the Canton of Graubünden (equipped with the latest technology (dual polarisation), commenced operation in 2016, and monitors the atmosphere in the inner Alpine region)

>*Open Data Product (Title):* **...** <br>
>*Data structure (Example file):* [...](...) <br>
>*Granularity:* ... (see [chapter 2.1.1.](#211-data-of-meteoswiss-data-granularity) for more details) <br>
>*Update frequency:* ... - see [chapter 2.1.2.](#212-structure-and-update-cycle) for more details! <br>
>*Format:* ... <br>
>*Volume (MB/GB/TB):* ... <br>
>*Network map:* ... <br>
>*Station metadata:* ... <br>
>*Parameter metadata:* [...](...) <br>
>*Additional remarks*: ... <br>


#### 2.4. Model data

#### 2.4.1. INCA data (nowcasting)
The INCA [nowcasting](https://www.meteoswiss.admin.ch/weather/warning-and-forecasting-systems/nowcasting.html) forecasts come in 2 versions for most parameters a) a short 0h- +6h version and an b) an extended 6h-+28/33h version.
Please be aware, that in the extended versions, the part after the first 6h comes from the COSMO-1E model, which means, that it is beeing updated only every 3h (00h, 03h, 06h, 09h etc. UTC). Only the first +6h are beeing updated according to the respective update frequency. 
For more information see the metadata in each NetCDF-File.

>*Open Data Product (Title):* **INCA Precipitation quantitative (based on CombiPrecip, RR)** <br>
>*Data structure (Example file):* [RR_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/RR_INCA_202106280700.nc) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 1.8 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 <br>

>*Open Data Product (Title):* **INCA Precipitation quantitative extended forecast (based on CombiPrecip, RR_ext)** <br>
>*Data structure (Example file):* see short forecast version <br>
>*Granularity:* 10min <br>
>*Update frequency:* 3h (00h, 03h, 06h, 09h etc. UTC) <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 20 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Precipitation qualitative (based on radar only, RP)** <br>
>*Data structure (Example file):* [RP_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/RP_INCA_202106280700.nc)  <br>
>*Granularity:* 5min <br>
>*Update frequency:* 5min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 3.5 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Precipitation qualitative extended forecast (based on radar only, RP_ext )** <br>
>*Data structure (Example file):* see short forecast version <br>
>*Granularity:* 5min <br>
>*Update frequency:* 3h (00h, 03h, 06h, 09h etc. UTC) <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 37 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Snowfall quantitative (based on CombiPrecip, RS)** <br>
>*Data structure (Example file):* [RS_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/RS_INCA_202106280700.nc) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 0.5 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Snowfall quantitative extended forecast (based on CombiPrecip, RS_ext)** <br>
>*Data structure (Example file):* see short forecast version  <br>
>*Granularity:* 10min <br>
>*Update frequency:* 3h (00h, 03h, 06h, 09h etc. UTC) <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 1.5 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Snowfall qualitative (based on radar only, PN)** <br>
>*Data structure (Example file):* [PN_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/PN_INCA_202106280700.nc) <br>
>*Granularity:* 5min <br>
>*Update frequency:* 5min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 0.7 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Snowfall qualitative extended forecast (based on radar only, PN_ext)** <br>
>*Data structure (Example file):* see short forecast version  <br>
>*Granularity:* 5min <br>
>*Update frequency:* 3h (00h, 03h, 06h, 09h etc. UTC) <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 2.9 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Precipitation type for RR in 5 classes rain, snow, snow-rain,freezing rain,rain&hail (hail first 30min only, PT)** <br>
>*Data structure (Example file):* [PT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/PT_INCA_202106280700.nc) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 0.7 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Precipitation type for RR_ext extended forecast in 5 classes rain, snow, snow-rain,freezing rain,rain&hail (hail first 30min only, PT_ext)** <br>
>*Data structure (Example file):* see short forecast version  <br>
>*Granularity:* 10min <br>
>*Update frequency:* 3h (00h, 03h, 06h, 09h etc. UTC) <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 4.5 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Precipitation type for RP in 5 classes rain, snow, snow-rain,freezing rain,rain&hail (hail first 30min only, NT)** <br>
>*Data structure (Example file):* [NT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/NT_INCA_202106280700.nc) <br>
>*Granularity:* 5min <br>
>*Update frequency:* 5min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 1.5 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Precipitation type for RP_ext extended forecast in 5 classes rain, snow, snow-rain,freezing rain,rain&hail (hail first 30min only, NT_ext)** <br>
>*Data structure (Example file):* see short forecast version  <br>
>*Granularity:* 5min <br>
>*Update frequency:* 3h (00h, 03h, 06h, 09h etc. UTC) <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 8.5 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA New Snow Accumulation 24h (SH_BK_24)** <br>
>*Data structure (Example file):* [SH_BK_24_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/SH_BK_24_INCA_202106280700.nc) <br>
>*Granularity:* 24h <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 20 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Snowfall line (ZS)** <br>
>*Data structure (Example file):* [ZS_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/ZS_INCA_202106280700.nc) <br>
>*Granularity:* 60min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 12.2 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Zero degree isotherm (Z0)** <br>
>*Data structure (Example file):* [Z0_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/Z0_INCA_202106280700.nc) <br>
>*Granularity:* 60min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 12.2 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA temperature (TT)** <br>
>*Data structure (Example file):* [TT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/TT_INCA_202106280700.nc) <br>
>*Granularity:* 60min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 12.5 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Temperature extended (TT_ext)** <br>
>*Data structure (Example file):* see short forecast version  <br>
>*Granularity:* 60min <br>
>*Update frequency:* 3h (00h, 03h, 06h, 09h etc. UTC) <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 42 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Dewpoint temperature (TD)** <br>
>*Data structure (Example file):* [TD_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/TD_INCA_202106280700.nc) <br>
>*Granularity:* 60min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 12.5 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Dewpoint temperature Extended (TD_Ext)** <br>
>*Data structure (Example file):* see short forecast version  <br>
>*Granularity:* 60min <br>
>*Update frequency:* 3h (00h, 03h, 06h, 09h etc. UTC) <br>
>*Format:* NetCDF <br>
>*Volume (MB):* ?? <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Soil surface temperature (TG)** <br>
>*Data structure (Example file):* [TG_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/TG_INCA_202106280700.nc) <br>
>*Granularity:* 60min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 12.5 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Relative sunshine duration (SU)** <br>
>*Data structure (Example file):* [SU_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca/SU_INCA_202106280700.nc) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 6.4 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA ** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* ?? <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA ** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 20 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA ** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 20 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA ** <br>
>*Data structure (Example file):* [https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv](https://github.com/MeteoSwiss/publication-opendata/blob/main/....csv) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 20 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

<!-- #### 2.4.3. COSMO/ICON data (forecasting)
... -->

#### 2.5. Grid data

#### 2.5.1. Spatial climate data  
[Overview of spatial climate products](https://www.meteoschweiz.admin.ch/dam/jcr:215c313a-dc13-4b67-bca0-dbd966597f9a/ProdDoc_Cover-dfie.pdf) <br>
The spatial climate data are statistically derived from surface data. 
The spatial climate data, which contain radiation and cloud cover parameters are derived from MeteoSat satellite data together with surface data. 
See the linked description files for each product for further information. 
For more information see also the metadata in each NetCDF-File.

>*Open Data Product (Title):* **Gridded precipitation data (RprelimD, RhiresD, RhiresM, RhiresY)** <br>
>*Detailed product document(s):* *[RprelimD](https://www.meteoswiss.admin.ch/dam/jcr:86ca15d3-2b56-4753-84fb-135e40d6a5a1/ProdDoc_RprelimD.pdf),  [RhiresD](https://www.meteoswiss.admin.ch/dam/jcr:4f51f0f1-0fe3-48b5-9de0-15666327e63c/ProdDoc_RhiresD.pdf), [RhiresM,RhiresY](https://www.meteoswiss.admin.ch/dam/jcr:d4f53a4a-d7f4-4e1e-a594-8ff4bfd1aca5/ProdDoc_RhiresM.pdf) <br>
>*Data structure (Example file):* [RhiresD.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/RhiresD_ch01h.swiss.lv95_202305010000_202305310000.nc), [RhiresM.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/RhiresM_ch01r.swiss.lv95_202305010000_202305010000.nc), [RhiresY.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/RhiresY_ch01r.swiss.lv95_202201010000_202201010000.nc) <br>
>*Granularity:* daily, monthly, yearly <br>
>*Update frequency:* according to granularity <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 1.1 for individual files, monthly files with daily data 13MB <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **Gridded temperature data (TabsD,TminD,TmaxD,TabsM,TminM,TmaxM,TabsY,TminY,TmaxY)** <br>
>*Detailed product document(s):* *[TabsD,TminD,TmaxD](https://www.meteoswiss.admin.ch/dam/jcr:818a4d17-cb0c-4e8b-92c6-1a1bdf5348b7/ProdDoc_TabsD.pdf), [TabsM, TabsY](https://www.meteoswiss.admin.ch/dam/jcr:33e26211-9937-4f80-80a3-09cfe54663bc/ProdDoc_TabsM.pdf) <br>
>*Data structure (Example file):* [TabsD.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/TabsD_ch01r.swiss.lv95_202305010000_202305310000.nc), [TabsM.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/TabsM_ch01r.swiss.lv95_202305010000_202305010000.nc), [TmaxM.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/TmaxM_ch01r.swiss.lv95_202305010000_202305010000.nc), [TminY.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/TminY_ch01r.swiss.lv95_202201010000_202201010000.nc)<br>
>*Granularity:* daily, monthly, yearly <br>
>*Update frequency:* according to granularity <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 1.1 for individual files, monthly files with daily data 13MB<br>
>*Additional remarks*: Coordinate System : Swiss LV95 EPSG:2056< <br>

>*Open Data Product (Title):* **Gridded relative sunshine duration data (SreldD,SrelM,SrelY)** <br>
>*Detailed product document(s):* *[SrelD](https://www.meteoswiss.admin.ch/dam/jcr:981891db-30d1-47cc-a2e1-50c270bdaf22/ProdDoc_SrelD.pdf), [SrelM,SrelY](https://www.meteoswiss.admin.ch/dam/jcr:94421f3c-47f3-46fa-9939-1d494a0ce5fe/ProdDoc_SrelM.pdf) <br>
>*Data structure (Example file):* [SrelD.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/SrelD_ch01r.swiss.lv95_202305010000_202305310000.nc), [SrelM.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/SrelM_ch01r.swiss.lv95_202305010000_202305010000.nc), [SrelY.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/SrelY_ch01r.swiss.lv95_202201010000_202201010000.nc) <br>
>*Granularity:* daily, monthly, yearly <br>
>*Update frequency:* according to granularity <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 1.1 for individual files, monthly files with daily data 13MB <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

Satellite derived gridded data 

>*Open Data Product (Title):* **Gridded global radiation (MSG.SIS.D, MSG.SIS.M, MSG.SIS.Y)** <br>
>*Detailed product document(s):* *[MSG.SIS.D,M,Y](https://www.meteoswiss.admin.ch/dam/jcr:b0bbcbac-1a17-481b-aea4-e87e56183613/ProdDoc_SIS.pdf)<br>
>*Data structure (Example file):* [MSG.SIS.D.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SIS.D_ch02.lonlat_20201206000000.nc), [MSG.SIS.M.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SIS.M_ch02.lonlat_20210401000000.nc), [MSG.SIS.Y.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SIS.Y_ch02.lonlat_20210101000000.nc) <br>
>*Granularity:* daily, monthly, yearly <br>
>*Update frequency:* according to granularity <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 0.1 <br>
>*Additional remarks*: Coordinate System :WGS84 lat/lon EPSG:4326 < <br>

>*Open Data Product (Title):* **Gridded diffuse radiation (MSG.SISDIF.D, MSG.SISDIF.M, MSG.SISDIF.Y)** <br>
>*Detailed product document(s):* *[MSG.SISDIF.D,M,Y](https://www.meteoswiss.admin.ch/dam/jcr:af0c491c-4bfc-4efd-bcee-5d019004afd1/ProdDoc_CFC.pdf)<br>
>*Data structure (Example file):* [MSG.SIS.D.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SIS.D_ch02.lonlat_20201206000000.nc), [MSG.SIS.M.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SIS.M_ch02.lonlat_20210401000000.nc), [MSG.SIS.Y.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SIS.Y_ch02.lonlat_20210101000000.nc) <br>
>*Granularity:* daily, monthly, yearly <br>
>*Update frequency:* according to granularity <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 0.1 <br>
>*Additional remarks*: Coordinate System :WGS84 lat/lon EPSG:4326< <br>

>*Open Data Product (Title):* **Gridded direct radiation (MSG.SISDIR.D, MSG.SISDIR.M, MSG.SISDIR.Y)** <br>
>*Detailed product document(s):* *[MSG.SISDIR.D,M,Y](https://www.meteoswiss.admin.ch/dam/jcr:b0bbcbac-1a17-481b-aea4-e87e56183613/ProdDoc_SIS.pdf) <br>
>*Data structure (Example file):* [MSG.SISDIR.D.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SISDIR.D_ch02.lonlat_20201206000000.nc), [MSG.SISDIR.M.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SISDIR.M_ch02.lonlat_20210401000000.nc), [MSG.SISDIR.Y.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.SISDIR.Y_ch02.lonlat_20210101000000.nc) <br>
>*Granularity:* daily, monthly, yearly <br>
>*Update frequency:* according to granularity <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 0.1 <br>
>*Additional remarks*: Coordinate System :WGS84 lat/lon EPSG:4326 < <br>

>*Open Data Product (Title):* **Gridded cloud fractional cover (MSG.CFC.D, MSG.CFC.M, MSG.CFC.Y)** <br>
>*Detailed product document(s):* *[MSG.CFC.D,M,Y](https://www.meteoswiss.admin.ch/dam/jcr:af0c491c-4bfc-4efd-bcee-5d019004afd1/ProdDoc_CFC.pdf) <br>
>*Data structure (Example file):* [MSG.CFC.D.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.CFC.D_ch02.lonlat_20201206000000.nc), [MSG.CFC.M.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.CFC.M_ch02.lonlat_20210401000000.nc), [MSG.CFC.Y.nc](https://github.com/MeteoSwiss/publication-opendata-spatial-climate-data/blob/main/msg.CFC.Y_ch02.lonlat_20210101000000.nc) <br>
>*Granularity:* daily, monthly, yearly <br>
>*Update frequency:* according to granularity <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 0.1 <br>
>*Additional remarks*: Coordinate System :WGS84 lat/lon EPSG:4326 < <br>


#### 2.5.2. Radar and combiprecip data
Radar data is beeing provided in the HDF5-Format which is the common exchange format for radar data.
See the metadata in each HDF5-File for further information. 
The radar data are divided into [basic radar data](https://www.meteoswiss.admin.ch/services-and-publications/service/weather-and-climate-products/basic-radar-products.html), [advanced radar data](https://www.meteoswiss.admin.ch/services-and-publications/service/weather-and-climate-products/radard-avanced.html) and [combiprecip](https://www.meteoswiss.admin.ch/dam/jcr:2691db4e-7253-41c6-a413-2c75c9de11e3/ProdDoc_CPC.pdf).

Basic radar data

>*Open Data Product (Title):* **Precip RZC** <br>
>*Data structure (Example file):* [Precip_RZC.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/Precip_RZC.h5) <br>
>*Granularity:* 5min <br>
>*Update frequency:* according to granularity <br>
>*Format:* HDF5 <br>
>*Volume (MB):* 0.2 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056  < <br>

>*Open Data Product (Title):** **<br>
>*Data structure (Example file):* []() <br>
>*Granularity:* 5min <br>
>*Update frequency:* according to granularity <br>
>*Format:* HDF5 <br>
>*Volume (MB):* 0.2 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056  < <br>

>*Open Data Product (Title):* **MAX-ECHO (CZC)** <br>
>*Data structure (Example file):* [MAX_ECHO_CZC.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/MAX_ECHO_CZC.h5) <br>
>*Granularity:* 5min <br>
>*Update frequency:* according to granularity <br>
>*Format:* HDF5 <br>
>*Volume (MB):* 0.2 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056  < <br>

>*Open Data Product (Title):* **ECHO TOP 45dBZ (EZC)** <br>
>*Data structure (Example file):* [ECHO_TOP_45dBZ](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/Echo_TOP_45dBZ_EZC.h5) <br>
>*Granularity:* 5min <br>
>*Update frequency:* according to granularity <br>
>*Format:* HDF5 <br>
>*Volume (MB):* 0.1 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056  < <br>


>*Open Data Product (Title):** ** <br>
>*Data structure (Example file):* []() <br>
>*Granularity:* 5min <br>
>*Update frequency:* according to granularity <br>
>*Format:* HDF5 <br>
>*Volume (MB):* 0.2 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056  < <br>

Advanced radar data

>*Open Data Product (Title):* **Probability of hail (POH)** <br>
>*Data structure (Example file):* [POH_BZC.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/POH_BZC.h5) <br>
>*Granularity:* 5min <br>
>*Update frequency:* according to granularity <br>
>*Format:* HDF5 <br>
>*Volume (MB):* 0.2 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056  < <br>



## 3. Questions for discussion with the open data user community
1. [Besides wind gusts (maximum wind speed) MeteoSwiss plans to only publish maximum and minimum (hourly, daily, monthly and yearly) for temperature, since these aggregations are widely used and used to be measured by separate instruments in the past. Do users want to have aggregated (calculated) maximum and minimum also for other parameters like pressure, humidity or soil parameters or will they calculate these themselves?](https://github.com/MeteoSwiss/publication-opendata/discussions/1)
2. [For sum parameters (precipitation, snow) MeteoSwiss plans to publish only one parameter per granularity. Do users want to have multi-hour (e.g. 6h, 12h, 24h) or multi-day (2d, 3d, 6d) aggregated sums or will they calculate these themselves?](https://github.com/MeteoSwiss/publication-opendata/discussions/2)
3. Is the mutation information (e.g. if a value is original, interpolated, automatically or manually corrected, aggregated etc.) or a value interesting for the user? If yes, in which format should we publish this data?
4. What kind of metadata for stations and parameters does the user community expect from MeteoSwiss? Are the examples below sufficient or does the OGD community need more metadata?
