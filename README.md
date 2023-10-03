*Version, status:* v1.0, draft <br>
*Maintainer:* Federal Office of Meteorology and Climatology MeteoSwiss, [OGD@MeteoSwiss project team](mailto:opendata@meteoswiss.ch)

[![GitHub commit](https://img.shields.io/github/last-commit/MeteoSwiss/publication-opendata)](https://github.com/MeteoSwiss/publication-opendata/commits/master)

# OGD@MeteoSwiss - Open Government Data

> **TL;DR** <br>
> Jump directly to the [overview of which data types are to be made available as Open Data](https://github.com/MeteoSwiss/publication-opendata/tree/master#21-overview-of-data-types-to-be-made-available-as-open-data). <br>
> Jump directly to the [questions on which we are asking the Open Data user community for feedback](https://github.com/MeteoSwiss/publication-opendata/tree/master#12-questions-to-the-open-data-user-community). <br>
<!-- > Jump directly to the [roadmap of MeteoSwiss' OGD service](https://github.com/MeteoSwiss/publication-opendata/tree/master#3-roadmap-of-meteoswiss-ogd-service). -->

## Table of contents

1. [Context and mission of the project](https://github.com/MeteoSwiss/publication-opendata/tree/master#1-context-and-mission-of-the-project)
    - 1.1. [Purpose of this repository](https://github.com/MeteoSwiss/publication-opendata/tree/master#11-purpose-of-this-repository)
    - 1.2. [Questions to the Open Data user community](https://github.com/MeteoSwiss/publication-opendata/tree/master#12-questions-to-the-open-data-user-community)
    - 1.3. [General contact point](https://github.com/MeteoSwiss/publication-opendata/tree/master#13-general-contact-point)
    <!-- - 1.4. [OGD Newsletter](https://github.com/MeteoSwiss/publication-opendata/tree/master#14-ogd-newsletter) -->
2. [Open Data products](https://github.com/MeteoSwiss/publication-opendata/tree/master#2-open-data-products)
    - 2.1. [Overview of data types to be made available as Open Data](https://github.com/MeteoSwiss/publication-opendata/tree/master#21-overview-of-data-types-to-be-made-available-as-open-data)  
    - 2.2. [General information on the data](https://github.com/MeteoSwiss/publication-opendata/tree/master#22-general-information-on-the-data)
        - 2.2.1. [Data granularity](https://github.com/MeteoSwiss/publication-opendata/tree/master#221-data-granularity)
        - 2.2.2. [Data structure and update cycle](https://github.com/MeteoSwiss/publication-opendata/tree/master#222-data-structure-and-update-cycle)
        - 2.2.3. [Time stamps and time intervals](https://github.com/MeteoSwiss/publication-opendata/tree/main#223-time-stamps-and-time-intervals)
        - 2.2.4. [Column separators, decimal dividers and missing values](https://github.com/MeteoSwiss/publication-opendata/tree/main#224-column-separators-decimal-dividers-and-missing-values)
    - 2.3. [Surface data](https://github.com/MeteoSwiss/publication-opendata/tree/master#23-surface-data)
        - 2.3.1. [Automatic weather stations (smn, smn-precip, smn-tower)](https://github.com/MeteoSwiss/publication-opendata/tree/main#231-automatic-weather-stations-smn-smn-precip-smn-tower)
        - 2.3.2. [Manual precipitation stations (nime, tot)](https://github.com/MeteoSwiss/publication-opendata/tree/main#232-manual-precipitation-stations-nime-tot)
        - 2.3.3. [Visual observations (obs)](https://github.com/MeteoSwiss/publication-opendata/tree/main#233-visual-observations-obs)
        - 2.3.4. [Climate stations "Swiss NBCN" (climate, climate-precip)](https://github.com/MeteoSwiss/publication-opendata/tree/main#234-climate-stations-swiss-nbcn-climate-climate-precip)
            - 2.3.4.1. [Records and extremes](https://github.com/MeteoSwiss/publication-opendata/tree/main#2341-records-and-extremes)
        - 2.3.5. [Swiss pollen monitoring stations (pollen)](https://github.com/MeteoSwiss/publication-opendata/tree/main#235-swiss-pollen-monitoring-stations-pollen)
        - 2.3.6. [Phenological observations (phenology)](https://github.com/MeteoSwiss/publication-opendata/tree/main#236-phenological-observations-phenology)
    - 2.4. [Atmosphere data](https://github.com/MeteoSwiss/publication-opendata/tree/main#24-atmosphere-data)
        - 2.4.1. [Radio soundings (radiosounding)](https://github.com/MeteoSwiss/publication-opendata/tree/main#241-radio-soundings-radiosounding)
    - 2.5. [Model data](https://github.com/MeteoSwiss/publication-opendata/tree/main#25-model-data)
        - 2.5.1. [INCA data (nowcasting)](https://github.com/MeteoSwiss/publication-opendata/tree/main#251-inca-data-nowcasting)
            - 2.5.1.1. [INCA precipitation - quantitative/qualitative](https://github.com/MeteoSwiss/publication-opendata/tree/main#2511-inca-precipitation---quantitativequalitative)
            - 2.5.1.2. [INCA precipitation type - rain, snow, snow-rain, freezing rain, rain&hail](https://github.com/MeteoSwiss/publication-opendata/tree/main#2512-inca-precipitation-type---rain-snow-snow-rain-freezing-rain-rainhail)
            - 2.5.1.3. [INCA snowfall - quantitative/qualitative](https://github.com/MeteoSwiss/publication-opendata/tree/main#2513-inca-snowfall---quantitativequalitative)
            - 2.5.1.4. [INCA snow accumulation & snowfall line](https://github.com/MeteoSwiss/publication-opendata/tree/main#2514-inca-snow-accumulation--snowfall-line)
            - 2.5.1.5. [INCA temperature](https://github.com/MeteoSwiss/publication-opendata/tree/main#2515-inca-temperature)
            - 2.5.1.6. [INCA relative sunshine duration](https://github.com/MeteoSwiss/publication-opendata/tree/main#2516-inca-relative-sunshine-duration)
        - 2.5.2. [COSMO/ICON data (forecasting)](https://github.com/MeteoSwiss/publication-opendata/tree/main#252-cosmoicon-data-forecasting)
        - 2.5.3. [Postprocessed local forecast data (data4web)](https://github.com/MeteoSwiss/publication-opendata/tree/main#253-postprocessed-local-forecast-data-data4web)
    - 2.6. [Grid data](https://github.com/MeteoSwiss/publication-opendata/tree/main#26-grid-data)
        - 2.6.1. [Spatial climate data](https://github.com/MeteoSwiss/publication-opendata/tree/main#261-spatial-climate-data)
            - 2.6.1.1. [Surface derived gridded data](https://github.com/MeteoSwiss/publication-opendata/tree/main#2611-surface-derived-grid-data)
            - 2.6.1.2. [Satellite derived gridded data](https://github.com/MeteoSwiss/publication-opendata/tree/main#2612-satellite-derived-grid-data)
        - 2.6.2. [Radar and combiprecip data](https://github.com/MeteoSwiss/publication-opendata/tree/main#262-Radar-and-combiprecip-data)
            - 2.6.2.1. [Basic radar data](https://github.com/MeteoSwiss/publication-opendata/tree/main#2621-basic-radar-data)
            - 2.6.2.2. [Advanced radar data](https://github.com/MeteoSwiss/publication-opendata/tree/main#2622-advanced-radar-data)
            - 2.6.2.3. [Combiprecip data](https://github.com/MeteoSwiss/publication-opendata/tree/main#2623-combiprecip-data)
    - 2.7. [Warning data](https://github.com/MeteoSwiss/publication-opendata/tree/main#27-warning-data)
3. [Roadmap of MeteoSwiss' OGD service](https://github.com/MeteoSwiss/publication-opendata/tree/master#3-roadmap-of-meteoswiss-ogd-service)


## 1. Context and mission of the project
In order to legally implement the [Federal Act on the use of electronic means for the performance of official duties' (EMBAG)](https://www.meteoswiss.admin.ch/about-us/remit-and-legal-mandate.html) the overall revision of the Ordinance on Meteorology and Climatology (MetV; SR 429.11) is now pending.

In the current year (2023) the necessary technical and organizational measures for the implementation of Open Government Data (OGD) at [MeteoSwiss](https://www.meteoswiss.admin.ch/about-us/portrait.html) are being tackled within the scope of a project.

> **Finding out, collecting, analysing and weighting user needs** is the central way for the project team to be able to offer good 'Open Data products'.
> Thank you very much for your attention and your openness to enter into an exchange with us on this matter.

According to the current schedule the implementation may be expected during early 2025.

### 1.1. Purpose of this repository
This repository is used by MeteoSwiss' project team to inform potential users interested in Open Data about the plans and to receive specific feedback from them on proposals.
1. [We describe the various 'Open Data products'](https://github.com/MeteoSwiss/publication-opendata/tree/main#2-open-data-products) being designed by MeteoSwiss' specialist data teams. That is: the **data structures, formats, denominations, update frequencies, volumes and other specifics**.
2. We are looking for your feedback on our proposals. To this end, **[we ask you specific questions](https://github.com/MeteoSwiss/publication-opendata/tree/main#12-questions-to-the-open-data-user-community)**.
3. Furthermore we are open to your questions. **Please [share them with us and the community by creating a public issue](https://github.com/MeteoSwiss/publication-opendata/issues/new)**, or [write us an email](https://github.com/MeteoSwiss/publication-opendata/tree/main#13-general-contact-point). You can find all issues - open and closed - sorted by update date [here](https://github.com/MeteoSwiss/publication-opendata/issues?q=is%3Aissue+sort%3Aupdated-desc).
4. MeteoSwiss' Open Data teams usually meet every second week to review and clarify the questions and feedback received, and ask questions back when necessary.

**Important note:**
- All information in this repository reflects the current state of work and is subject to change.

### 1.2. Questions to the Open Data user community
These are the **current questions to the Open Data user community** on which we are asking for feedback:

| Data category | ID | Question | Status | Since date |
| :------------ | :- | :------- | :----- | :--------- |
| **Surface** | S1 | [Aggregated (calculated) maximum and minimum?](https://github.com/MeteoSwiss/publication-opendata/discussions/1) | Open for feedback | 2023-10-02 |
| **Surface** | S2 | [Multi-hour or multi-day aggregated sums?](https://github.com/MeteoSwiss/publication-opendata/discussions/22) | Open for feedback | 2023-10-02 |
| **Surface** | S3 | [Mutation information?](https://github.com/MeteoSwiss/publication-opendata/discussions/24) | Open for feedback | 2023-08-02 |
| **Surface** | S4 | [Metadata for stations and parameters?](https://github.com/MeteoSwiss/publication-opendata/discussions/27) | Open for feedback | 2023-10-02 |
| **Atmosphere** | A0 | no question yet | ... | ... |
| **Model** | M0 | no question yet | ... | ... |
| **Grid** | G0 | no question yet | ... | ... |

### 1.3. General contact point
If you have any questions, please contact the project team: [opendata(at)meteoswiss.ch](mailto:opendata@meteoswiss.ch)

<!-- ### 1.4. OGD newsletter
Don't miss any updates on Open Government Data from MeteoSwiss. [Subscribe] to the OGD newsletter. Or send an email to: [ogd-news(at)news.meteoswiss.ch](ogd-news@news.meteoswiss.ch) with the subject: JOIN ogd_list -->

## 2. Open Data products

### 2.1. Overview of data types to be made available as Open Data
MeteoSwiss operates an extensive monitoring network, both on the ground (surface stations) and in the atmosphere, that enables it to collect round-the-clock meteorological data for the whole of Switzerland. These data form the basis for making weather forecasts, issuing bad weather warnings, and analysing climate change. Furthermore MeteoSwiss operates a weather model for forecasting and also generates gridded data sets.

This is the **current status of the clarifications** as to which data types can be made available (and how) under an Open Data license by MeteoSwiss, and which not:

| Data category | can be made available as Open Data | in clarification if/how | cannot be made available as Open Data - with reasons) | 
| :------------ | :--------------------------------- | :---------------------- | :---------------------------------------------------- |
| [**Surface**](https://github.com/MeteoSwiss/publication-opendata/tree/main#23-surface-data) | [Automatic weather stations](https://github.com/MeteoSwiss/publication-opendata/tree/main#231-automatic-weather-stations-smn-smn-precip-smn-tower) | <!-- [Aerosol measurements](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/aerosol-measurements.html) --> | [Aviation weather](https://www.meteoswiss.admin.ch/services-and-publications/service/weather-and-climate-products/aviation-weather.html) - These data are collected on behalf of and financed by professional aviation |
|  | [Manual precipitation stations](https://github.com/MeteoSwiss/publication-opendata/tree/main#232-manual-precipitation-stations-nime-tot) |  |  |
|  | [Visual observations](https://github.com/MeteoSwiss/publication-opendata/tree/main#233-visual-observations-obs) |  |  |
|  | [Climate stations "Swiss NBCN"](https://github.com/MeteoSwiss/publication-opendata/tree/main#234-climate-stations-swiss-nbcn-climate-climate-precip) | [Records and extremes](https://github.com/MeteoSwiss/publication-opendata/tree/main#2341-records-and-extremes) |  |
|  | [Swiss pollen monitoring stations](https://github.com/MeteoSwiss/publication-opendata/tree/main#235-swiss-pollen-monitoring-stations-pollen) |  |  |
|  | [Phenological observations](https://github.com/MeteoSwiss/publication-opendata/tree/main#236-phenological-observations-phenology) |  |  |
| [**Atmosphere**](https://github.com/MeteoSwiss/publication-opendata/tree/main#24-atmosphere-data) | [Radio soundings](https://github.com/MeteoSwiss/publication-opendata/tree/main#241-radio-soundings-radiosounding) | [Windprofiler](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/windprofiler.html) | [Observations from aircraft](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/observations-from-aircraft.html) - Data does not belong to MeteoSwiss |
|  |  | [LIDAR and ceilometers](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/lidar-and-ceilometers.html) | [Satellite observations](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/satellite-observations.html) - Data does not belong to MeteoSwiss |
|  |  | [Microwave radiometry](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/microwave-radiometry.html) | [Lightning detection network](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/lightning-detection-network.html) - Data does not belong to MeteoSwiss |
|  |  | [Ozone measurements](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/ozone-measurements.html) |  |
|  |  | [Radiation monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/atmosphere/radiation-monitoring-network.html) |  |
| [**Model**](https://github.com/MeteoSwiss/publication-opendata/tree/main#25-model-data) | [INCA data (nowcasting)](https://github.com/MeteoSwiss/publication-opendata/tree/main#251-inca-data-nowcasting) |  |  |
|  |  | [COSMO/ICON data (forecasting)](https://github.com/MeteoSwiss/publication-opendata/tree/main#252-cosmoicon-data-forecasting) |  |
|  | [Postprocessed local forecast data (data4web)](https://github.com/MeteoSwiss/publication-opendata/tree/main#253-postprocessed-local-forecast-data-data4web) |  |  |
| [**Grid**](https://github.com/MeteoSwiss/publication-opendata/tree/main#26-grid-data) | [Spatial climate data](https://github.com/MeteoSwiss/publication-opendata/tree/main#261-Spatial-climate-data) |  |  |
|  | [Radar and compiprecip data](https://github.com/MeteoSwiss/publication-opendata/tree/main#262-Radar-and-combiprecip-data) |  |  |
| [**Warning**](https://github.com/MeteoSwiss/publication-opendata/tree/main#27-warning-data) |  | Weather hazard data |  |


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
SwissMetNet, the [automatic measurement network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html) of MeteoSwiss, comprises about 160 automatic stations with a full measurement program (`smn`). These stations deliver a multitude of current data on weather and climate in Switzerland every ten minutes. The network is supplemented by around 100 automatic precipitation stations (`smn-precip`). Together, these stations form the basis for the creation of reliable local weather forecasts as well as severe weather and flood warnings. Additionally MeteoSwiss operates three tower stations at 150m to 230m above ground for boundry layer measurements (`smn-tower`).

| *Dataset title*                | Measurement data from automatic weather stations |
| :----------------------------- | :----------------------------------------------- |
| *Data structure*               | see example files: [`smn`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn), [`smn-precip`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn-precip), [`smn-tower`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/automatic-weather-stations/smn-tower) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `T`, `H`, `D`, `M` and `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`), daily (`recent`) or hourly (`now`) |
| *Format*                       | `CSV` |
| *Volume*                       | ≤5.3 MB |
| *Visualisation*                | [SwissMetNet network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-automatisch&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-automatisch/ch.meteoschweiz.messnetz-automatisch_en.csv) |
| *Parameter metadata*           | see parameter files: [`smn-T`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-T.csv), [`smn-H`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-H.csv), [`smn-D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-D.csv), [`smn-M`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-M.csv) and [`smn-Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-smn-Y.csv)
| *Additional remarks*           | One file per station. |

#### 2.3.2. Manual precipitation stations (`nime`, `tot`)
In addition to its automatic precipitation measurements, MeteoSwiss operates a [manual precipitation monitoring network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html). Measurements are taken once a day and transmitted to MeteoSwiss via SMS. The network comprises 243 locations, 190 stations measure rainfall and  and 53 stations measure  only (`nime`). Due to their long-series measurements, they are of great climatological significance. In mountainous areas that are difficult to access, around 57 totalisers are used which record the volume of precipitation for an entire year (`tot`).

| *Dataset title*                | Measurement data from manual precipitation stations |
| :----------------------------- | :-------------------------------------------------- |
| *Data structure*               | see example files: [`nime`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/manual-precipitation-stations-nime), [`tot`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/manual-precipitation-stations-tot) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`), daily (`recent`) or hourly (`now`) |
| *Format*                       | `CSV` |
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
| *Format*                       | `CSV` |
| *Volume*                       | ≤0.04 MB |
| *Visualisation*                | [OBS network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-manuell&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-beobachtungen/ch.meteoschweiz.messnetz-beobachtungen_en.csv) |
| *Parameter metadata*           | see parameter file: [`obs-T`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-obs-T.csv) |
| *Additional remarks*           | One file per station. |

#### 2.3.4. Climate stations "Swiss NBCN" (`climate`, `climate-precip`)
The [Swiss National Basic Climatological Network "Swiss NBCN"](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/swiss-national-basic-climatological-network.html) connects the major ground-based stations within the MeteoSwiss monitoring network. It consists of 29 climate monitoring stations and 46 precipitation stations. The measurement series available in digital form for temperature, precipitation and hours of sunshine date back, in some cases, to the mid-nineteenth century.

| *Dataset title*                | Measurement data from the Swiss National Basic Climatological Network |
| :----------------------------- | :-------------------------------------------------------------------- |
| *Data structure*               | see example files: [`climate`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/climate-stations-swiss-nbcn-climate), [`climate-precip`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/climate-stations-swiss-nbcn-climate-precip) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `D`, `M` and `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`), daily (`recent`) or hourly (`now`) |
| *Format*                       | `CSV` |
| *Volume*                       | ≤0.9 MB |
| *Visualisation*                | [CLIMATE network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-klima&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-klima/ch.meteoschweiz.messnetz-klima_en.csv) |
| *Parameter metadata*           | see parameter files: [`climate-D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-climate-D.csv), [`climate-M`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-climate-M.csv) and [`climate-Y`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-climate-Y.csv) |
| *Additional remarks*           | One file per station. |

<!-- ##### 2.3.4.1 Records and extremes
Additionally the top 10 records of every climate station and the overall records can be downloaded per parameter separately.

| *Dataset title*                | ... |
| :----------------------------- | :----------------------------- |
| *Data structure*               | see example file: [`...`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/...) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`) |
| *Format*                       | `CSV` |
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
| *Format*                       | `CSV` |
| *Volume*                       | 0.6 MB |
| *Visualisation*                | [POLLEN network map](https://www.meteoswiss.admin.ch/services-and-publications/applications/measurement-values-and-measuring-networks.html#param=messnetz-pollen&lang=en) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-pollen/ch.meteoschweiz.messnetz-pollen_en.csv) |
| *Parameter metadata*           | see parameter files: [`pollen-H`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-pollen-H.csv) and [`pollen-D`](https://github.com/MeteoSwiss/publication-opendata/blob/main/data-surface/metadaten-parameter/metadata-parameter-pollen-D.csv) |
| *Additional remarks*           | One file per station. |

#### 2.3.6. Phenological observations (`phenology`)
The [Swiss Phenology Network](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/swiss-phenology-network.html) consists of 160 stations. Some 26 different plant species are observed in order to describe the vegetation development. On the basis of this information, it is possible to investigate the impact of climate change on the vegetation. The observations also serve to generate forecasting models for the start of flowering.

| *Dataset title*                | Measurement data from the Swiss Phenology NBetwork |
| :----------------------------- | :-------------------------------------------------------- |
| *Data structure*               | see example files: [`phenology`](https://github.com/MeteoSwiss/publication-opendata/tree/main/data-surface/phenology) |
| [*Data granularity*](https://github.com/MeteoSwiss/publication-opendata/tree/main#221-data-granularity) | `Y` |
| [*Update frequency*](https://github.com/MeteoSwiss/publication-opendata/tree/main#222-data-structure-and-update-cycle) | yearly (`historical`) or daily (`recent`) |
| *Format*                       | `CSV` |
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
| *Format*                       | `CSV` |
| *Volume*                       | 0.02 MB |
| *Visualisation*                | [Emagram](https://www.meteoswiss.admin.ch/services-and-publications/applications/radio-soundings.html#tab=radio-soundings-emagram) |
| *Station metadata*             | see [station list (CSV)](https://data.geo.admin.ch/ch.meteoschweiz.messnetz-atmosphaere/ch.meteoschweiz.messnetz-atmosphaere_en.csv) |
| *Parameter metadata*           | see [parameter file](https://github.com/MeteoSwiss/publication-opendata/blob/main/atmosphere/radiosounding-PAY-metadata) |
| *Additional remarks*           | One file per station. |

### 2.5. Model data

> Jump directly to 2.5.2. [COSMO/ICON data (forecasting)](https://github.com/MeteoSwiss/publication-opendata/tree/main#252-cosmoicon-data-forecasting). <br>
> Jump directly to 2.5.3. [Postprocessed local forecast data (data4web)](https://github.com/MeteoSwiss/publication-opendata/tree/main#253-postprocessed-local-forecast-data-data4web). <br>

#### 2.5.1. INCA data (nowcasting)
The INCA [nowcasting](https://www.meteoswiss.admin.ch/weather/warning-and-forecasting-systems/nowcasting.html) forecasts come in 2 versions for most parameters a) a short 0h- +6h version and an b) an extended 6h-+28/33h version.
Please be aware, that in the extended versions, the part after the first 6h comes from the COSMO-1E model, which means, that it is beeing updated only every 3h (00h, 03h, 06h, 09h etc. UTC). Only the first +6h are beeing updated according to the respective update frequency. 
For more information see the metadata in each NetCDF-File.

##### 2.5.1.1. INCA precipitation - quantitative/qualitative
| *Dataset title*                | INCA Precipitation quantitative (based on CombiPrecip, RR) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [RR_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/RR_INCA_202106280700.nc) |
| *Data granularity*             | Every 10min |
| *Update frequency*             | Every 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 1.7 MB |
| *Visualisation*                | [Precipitation](https://www.meteoswiss.admin.ch/services-and-publications/applications/precipitation.html) |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Precipitation quantitative extended forecast (based on CombiPrecip, RR_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version |
| *Data granularity*             | Every 10min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 20 MB |
| *Visualisation*                | ... |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Precipitation qualitative (based on radar only, RP) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [RP_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/RP_INCA_202106280700.nc) |
| *Data granularity*             | Every 5min |
| *Update frequency*             | Every 5min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 3.1 MB |
| *Visualisation*                | [Precipitation](https://www.meteoswiss.admin.ch/services-and-publications/applications/precipitation.html) |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Precipitation qualitative extended forecast (based on radar only, RP_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version |
| *Data granularity*             | Every 5min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 37 MB |
| *Visualisation*                | ... |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.5.1.2. INCA precipitation type - rain, snow, snow-rain, freezing rain, rain&hail
| *Dataset title*                | INCA Precipitation type for RR in 5 classes rain, snow, snow-rain, freezing rain, rain&hail (hail first 30min only, PT) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [PT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/PT_INCA_202106280700.nc) |
| *Data granularity*             | Every 10min |
| *Update frequency*             | Every 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.7 MB |
| *Visualisation*                | [Precipitation](https://www.meteoswiss.admin.ch/services-and-publications/applications/precipitation.html) |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Precipitation type for RR_ext extended forecast in 5 classes rain, snow, snow-rain, freezing rain, rain&hail (hail first 30min only, PT_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version |
| *Data granularity*             | Every 10min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 4.5 MB |
| *Visualisation*                | ... |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Precipitation type for RP in 5 classes rain, snow, snow-rain, freezing rain, rain&hail (hail first 30min only, NT) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | [NT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/NT_INCA_202106280700.nc) |
| *Data granularity*             | Every 5min |
| *Update frequency*             | Every 5min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 1.4 MB |
| *Visualisation*                | ... |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Precipitation type for RP_ext extended forecast in 5 classes rain, snow, snow-rain, freezing rain, rain&hail (hail first 30min only, NT_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version |
| *Data granularity*             | Every 5min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 8.5 MB |
| *Visualisation*                | ... |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.5.1.3. INCA snowfall - quantitative/qualitative
| *Dataset title*                | INCA Snowfall quantitative (based on CombiPrecip, RS) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [RS_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/RS_INCA_202106280700.nc) |
| *Data granularity*             | Every 10min |
| *Update frequency*             | Every 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.4 MB |
| *Visualisation*                | ... |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Snowfall quantitative extended forecast (based on CombiPrecip, RS_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version |
| *Data granularity*             | Every 10min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 1.5 MB |
| *Visualisation*                | ... |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Snowfall qualitative (based on radar only, PN) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see example file: [PN_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/PN_INCA_202106280700.nc) |
| *Data granularity*             | Every 5min |
| *Update frequency*             | Every 5min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.6 MB |
| *Visualisation*                | ... |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

| *Dataset title*                | INCA Snowfall qualitative extended forecast (based on radar only, PN_ext) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | see short forecast version |
| *Data granularity*             | Every 5min |
| *Update frequency*             | 3h (00h, 03h, 06h, 09h etc. UTC) |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 2.9 MB |
| *Visualisation*                | ... |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

##### 2.5.1.4. INCA snow accumulation & snowfall line

| *Dataset title*                | INCA New Snow Accumulation 24h (SH_BK_24) |
| :----------------------------- | :---------------------------------------- |
| *Data structure*               | [SH_BK_24_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/SH_BK_24_INCA_202106280700.nc) |
| *Data granularity*             | 24h |
| *Update frequency*             | 10min |
| *Format*                       | [`NetCDF`](https://www.unidata.ucar.edu/software/netcdf/) |
| *Volume*                       | 0.04 MB |
| *Visualisation*                | ... |
| *Station metadata*             | ... |
| *Parameter metadata*           | ... |
| *Additional remarks*           | Coordinate System: Swiss LV95 EPSG:2056 |

>*Open Data Product (Title):* **INCA Snowfall line (ZS)** <br>
>*Data structure (Example file):* [ZS_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/ZS_INCA_202106280700.nc) <br>
>*Granularity:* 60min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 12.2 MB <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

##### 2.5.1.5. INCA temperature

>*Open Data Product (Title):* **INCA Zero degree isotherm (Z0)** <br>
>*Data structure (Example file):* [Z0_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/Z0_INCA_202106280700.nc) <br>
>*Granularity:* 60min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 12.2 MB <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA temperature (TT)** <br>
>*Data structure (Example file):* [TT_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/TT_INCA_202106280700.nc) <br>
>*Granularity:* 60min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 12.2 MB <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Temperature extended (TT_ext)** <br>
>*Data structure (Example file):* see short forecast version  <br>
>*Granularity:* 60min <br>
>*Update frequency:* 3h (00h, 03h, 06h, 09h etc. UTC) <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 42 MB <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Dewpoint temperature (TD)** <br>
>*Data structure (Example file):* [TD_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/TD_INCA_202106280700.nc) <br>
>*Granularity:* 60min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 12.2 MB <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Dewpoint temperature Extended (TD_Ext)** <br>
>*Data structure (Example file):* see short forecast version  <br>
>*Granularity:* 60min <br>
>*Update frequency:* 3h (00h, 03h, 06h, 09h etc. UTC) <br>
>*Format:* NetCDF <br>
>*Volume (MB):* ?? <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

>*Open Data Product (Title):* **INCA Soil surface temperature (TG)** <br>
>*Data structure (Example file):* [TG_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/TG_INCA_202106280700.nc) <br>
>*Granularity:* 60min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 12.5 MB <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

##### 2.5.1.6. INCA relative sunshine duration

>*Open Data Product (Title):* **INCA Relative sunshine duration (SU)** <br>
>*Data structure (Example file):* [SU_INCA_202106280700.nc](https://github.com/MeteoSwiss/publication-opendata-inca-data-nowcasting/blob/main/SU_INCA_202106280700.nc) <br>
>*Granularity:* 10min <br>
>*Update frequency:* 10min <br>
>*Format:* NetCDF <br>
>*Volume (MB):* 6.4 MB <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056 < <br>

#### 2.5.2. COSMO/ICON data (forecasting)
Proposal in preparation ... 


#### 2.5.3. Postprocessed local forecast data (data4web)
The postprocessed forecast data is based on a mix of different models (INCA, COSMO-1E, COSMO-E2, ECMWF) and is available for all ZIP-Codes, SMN-Stations and selected POI in the mountains as punctual data. 
The forecast ist available for the time period of +0h - +192h and is being updated hourly. 
This is the same forecast we provide in the MeteoSwiss-App and on our website for each ZIP-code. 

For each parameter there is a single file. 
Here we provide only a few parameters for review. 

As for the geolocation of the data, the following metadata-files are beeing provided for mapping of the data: 

a) ZIP-code locations [Data4Web_legend_PLZ.txt] <br>
b) SMN-Stations and POI locations [Data4Web_legend_POI_Stations.txt] <br>

>*Open Data Product (Title):* **Hourly average temperature** <br>
>*Data structure (Example file):* [VNUT12.LSSX.202309271300.tre200b0.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessing\) <br>
>*Granularity:* hourly<br>
>*Update frequency:* hourly <br>
>*Format:* CSV <br>
>*Volume (MB):* 30 <br>
>*Additional remarks*: Unit: °C < <br>


>*Open Data Product (Title):* **Hourly sunshine duration** <br>
>*Data structure (Example file):* [VNUT12.LSSX.202309271300.spr100h0.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessing\) <br>
>*Granularity:* hourly<br>
>*Update frequency:* hourly <br>
>*Format:* CSV <br>
>*Volume (MB):* 30 <br>
>*Additional remarks*: Unit: Minutes < <br>


>*Open Data Product (Title):* **Hourly precipitation sum** <br>
>*Data structure (Example file):* [VNUT12.LSSX.202309271300.rre150b0.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessing\) <br>
>*Granularity:* hourly<br>
>*Update frequency:* hourly <br>
>*Format:* CSV <br>
>*Volume (MB):* 30 <br>
>*Additional remarks*: mm or l/m2 < <br>


>*Open Data Product (Title):* **Daily Temperature minimum** <br>
>*Data structure (Example file):* [VNUT12.LSSX.202309271300.tre200dn.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessing\) <br>
>*Granularity:* hourly<br>
>*Update frequency:* hourly <br>
>*Format:* CSV <br>
>*Volume (MB):* 0.3 <br>
>*Additional remarks*: Unit: °C < <br>

>*Open Data Product (Title):* **Daily temperature maximum** <br>
>*Data structure (Example file):* [VNUT12.LSSX.202309271300.tre200dx.csv](https://github.com/MeteoSwiss/publication-opendata-postprocessing\) <br>
>*Granularity:* hourly<br>
>*Update frequency:* hourly <br>
>*Format:* CSV <br>
>*Volume (MB):* 0.3 <br>
>*Additional remarks*: Unit: °C < <br>



### 2.6. Grid data

#### 2.6.1. Spatial climate data  
[Overview of spatial climate products](https://www.meteoschweiz.admin.ch/dam/jcr:215c313a-dc13-4b67-bca0-dbd966597f9a/ProdDoc_Cover-dfie.pdf) <br>
The spatial climate data are statistically derived from surface data. 
The spatial climate data, which contain radiation and cloud cover parameters are derived from MeteoSat satellite data together with surface data. 
See the linked description files for each product for further information. 
For more information see also the metadata in each NetCDF-File.

##### 2.6.1.1. Surface derived grid data

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

##### 2.6.1.2. Satellite derived grid data

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

#### 2.6.2. Radar and combiprecip data
Supplementing the conventional precipitation measurements taken at ground level meteorological stations, MeteoSwiss operates a network of five weather radar stations which record every type of precipitation and storms in real time, are fully automated and, between them, cover the whole of Switzerland.

The sites are
- Albis near Zurich (equipped with the latest technology (dual polarisation) in 2012, monitors the atmosphere of the whole of northern Switzerland)
- Monte Lema in the Canton of Ticino (equipped with the latest technology (dual polarisation) in 2011, monitors the atmosphere of the whole of southern Switzerland)
- La Dôle near Geneva (equipped with the latest technology (dual polarisation) in 2011)
- Pointe de la Plaine Morte in the Canton of Valais (equipped with the latest technology (dual polarisation), commenced operation in 2014 and monitors the atmosphere in the inner Alpine region)
- the Weissfluhgipfel in the Canton of Graubünden (equipped with the latest technology (dual polarisation), commenced operation in 2016, and monitors the atmosphere in the inner Alpine region)

Radar data is beeing provided in the HDF5-Format which is the common exchange format for radar data.
See the metadata in each HDF5-File for further information. 
The radar data are divided into [basic radar data](https://www.meteoswiss.admin.ch/services-and-publications/service/weather-and-climate-products/basic-radar-products.html), [advanced radar data](https://www.meteoswiss.admin.ch/services-and-publications/service/weather-and-climate-products/radard-avanced.html) and [combiprecip](https://www.meteoswiss.admin.ch/dam/jcr:2691db4e-7253-41c6-a413-2c75c9de11e3/ProdDoc_CPC.pdf).

##### 2.6.2.1. Basic radar data

>*Open Data Product (Title):* **Precip RZC** <br>
>*Data structure (Example file):* [Precip_RZC.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/Precip_RZC.h5) <br>
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

##### 2.6.2.2. Advanced radar data

>*Open Data Product (Title):* **Probability of hail (POH)** <br>
>*Data structure (Example file):* [POH_BZC.h5](https://github.com/MeteoSwiss/publication-opendata-radar-and-combiprecip-data/blob/main/POH_BZC.h5) <br>
>*Granularity:* 5min <br>
>*Update frequency:* according to granularity <br>
>*Format:* HDF5 <br>
>*Volume (MB):* 0.2 <br>
>*Additional remarks*: Coordinate System :Swiss LV95 EPSG:2056  < <br>

##### 2.6.2.3. Combiprecip data
Proposal in preparation ... 

### 2.7. Warning data
In clarification if/how can be made available as open data.

## 3. Roadmap of MeteoSwiss' OGD service
In preparation ...

<!-- https://app.productplan.com/G_PR7ExN/views/1164487/?layout=timeline -->
