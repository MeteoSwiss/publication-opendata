# OGD@MeteoSwiss - Open Government Data

## 1. Context and mission ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/context-and-purpose-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/context-and-purpose-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/context-and-purpose-IT))
In order to legally implement the [Federal Act on the use of electronic means for the performance of official duties' (EMBAG)](https://www.meteoswiss.admin.ch/about-us/remit-and-legal-mandate.html) the overall revision of the Ordinance on Meteorology and Climatology (MetV; SR 429.11) is now pending. In the current year (2023) the necessary technical and organizational measures for the implementation of OGD at MeteoSwiss are being tackled within the scope of a project.

### 1.1. Purpose of this repository
This repository is used by MeteoSwiss to inform potential users interested in open data about the plans and to receive specific feedback from them on proposals. **We describe below the open data products being designed by the various interdisciplinary data teams.** That is: the **data structures, formats, denominations, update frequencies, volumes and other specifics.**

All information reflects the current state of work and is subject to change. Finding out, collecting, analysing and weighting user needs is the central way for MeteoSwiss to be able to offer good open data products.

Thank you very much for your attention and openness to enter into an exchange with us for this purpose.

### 1.2. General contact point
If you have any questions, please contact the project core team: [opendata@meteoswiss.ch](mailto:opendata@meteoswiss.ch)

## 2. Open data products ([DE](https://github.com/MeteoSwiss/publication-opendata/blob/main/opendata-products-DE), [FR](https://github.com/MeteoSwiss/publication-opendata/blob/main/opendata-products-FR), [IT](https://github.com/MeteoSwiss/publication-opendata/blob/main/opendata-products-IT))

<!-- Tabelle mit 4 sprachen in spalten, statt Übersetzungen in Files? -->

- publication-opendata
     - [surface](https://github.com/MeteoSwiss/publication-opendata/tree/master#21-surface)
        - ~~aviation~~
        - smn (automatic-measurements)
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

### 2.1. Surface

#### 2.1.1. General description
This category/type of data is about ...

#### 2.1.2. Open questions to users
1. ...

#### 2.1.3. smn (automatic-measurements)

#### 2.1.3.1.  

Data structures, formats, granularities, update frequencies

>*Open Data Product (Title):* **10-Minuten-SMN-Werte-...** <br>
>*Data structure (Example file):* [https://github.com/openZH/covid_19/](https://github.com/MeteoSwiss/publication-opendata/blob/main/smn-10min-now.csv) <br>
>*Granularity:*  <br>
>*Format:* csv <br>

>*Additional remark*: [Link to deprecated dataset (data structure has changed)](https://github.com/openZH/covid_19/blob/master/fallzahlen_kanton_total_csv/ )

volumes and other specifics

#### 2.1.4. Metadata

| Field Name          | Description                                | Format     | Note |
|---------------------|--------------------------------------------|------------|------|
| __date__              | Date of notification                       | YYYY-MM-DD | |
| __time__                 | Time of notification                       | HH:MM      | |
| __abbreviation_canton_and_fl__  | Abbreviation of the reporting canton       | Text       | |
| __ncumul_tested__      | Reported number of tests performed as of date| Number     | Irrespective of canton of residence |
| __ncumul_conf__          | Reported number of confirmed cases as of date| Number     | Only cases that reside in the current canton |
| __new_hosp__        | new hospitalisations since last date | Number     | Irrespective of canton of residence |
| __current_hosp__       | Reported number of hospitalised patients on date | Number     | Irrespective of canton of residence |
| __current_icu__       | Reported number of hospitalised patients in ICUs on date| Number     | Irrespective of canton of residence |
| __current_vent__        | Reported number of patients requiring invasive ventilation on date | Number     | Irrespective of canton of residence |
| __ncumul_released__     |Reported number of patients released from hospitals or reported recovered as of date| Number     | Irrespective of canton of residence |
| __ncumul_deceased__     |Reported number of deceased as of date| Number     | Only cases that reside in the current canton |
| __source__              | Source of the information                  | href       | |
| __current_isolated__       | Reported number of isolated persons on date          | Number       | Infected persons, who are not hospitalised |
| __current_quarantined__    | Reported number of quarantined persons on date       | Number       | Persons, who were in 'close contact' with an infected person, while that person was infectious, and are not hospitalised themselves |
| __current_quarantined_riskareatravel__    | Reported number of quarantined persons on date       | Number       | People arriving in Switzerland from [certain countries and areas](https://www.bag.admin.ch/bag/en/home/krankheiten/ausbrueche-epidemien-pandemien/aktuelle-ausbrueche-epidemien/novel-cov/empfehlungen-fuer-reisende/quarantaene-einreisende.html), who are required to go into quarantine.  |


