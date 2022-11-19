# Introduction

The purpose of this project is to investigate the relationship between local weather trends and vehicle accidents in the city of Kelowna.


# Data Source

## Weather Data

Weather data was obtained from the [Government of Canada website](https://climate.weather.gc.ca/). The data used in this report was collected from [station \#51117](https://climate.weather.gc.ca/climate_data/daily_data_e.html?StationID=51117) (Kelowna UBCO). Historical weather data can be downloaded in bulk from the Government of Canada meteorological database using the `wget` tool. The [command](https://drive.google.com/drive/folders/1WJCDEU34c60IfOnG4rv5EPZ4IhhW9vZH) for downloading the data used in this report is:

> ``for year in `seq 2017 2021`;do for month in `seq 1 12`;do wget --content-disposition "https://climate.weather.gc.ca/climate_data/bulk_data_e.html?format=csv&stationID=51117&Year=${year}&Month=${month}&Day=14&timeframe=1&submit= Download+Data" ;done;done``

## Crash Data

Crash data was obtained from the Insurance Corporation of British Columbia's ([ICBC](https://icbc.com/about-icbc/newsroom/Pages/Statistics.aspx)) public [Tableau profile](https://public.tableau.com/app/profile/icbc/viz/PublicDataset-ICBCReportedCrashesSouthernInterior/ICBCReportedCrashes-SouthernInterior). Extracted data included the municipalities of Kelowna and West Kelowna (formerly "Westbank").


# Data Description

## Weather data

Variable information/data dictionary is available on the Government of Canada [website](https://climate.weather.gc.ca/glossary_e.html). Block quotes in this section are from said website.

### Longitude (x)

Longitude coordinate of the weather station.

### Latitude (y)

Latitute coordinate of the weather station.

### Station Name

> The station name is the official name of any meteorological station in the National Climate Archive as administered by the Meteorological Service of Canada (MSC).

### Climate ID

An ID number associated with each meteorological station.

> The first digit assigned identifies the province where the second and third digits identify the climatological district within the province.

### Date/Time (LST)

Date and time that the weather conditions were recorded.

> The Local Standard Time (LST) is used for observation purposes and is that of the standard time zone in which the station is located, whether or not "daylight saving time" is adopted for other purposes. In Canada, Local Standard Time is commonly used for archiving surface weather observations.

The LST in Kelowna is Pacific Standard Time.

### Temp (°C)

The recorded air temperature in degrees Celcius.

### Dew Point Temp (°C)

> The dew point temperature in degrees Celsius (°C), a measure of the humidity of the air, is the temperature to which the air would have to be cooled to reach saturation with respect to liquid water. Saturation occurs when the air is holding the maximum water vapour possible at that temperature and atmospheric pressure.

### Rel Hum (%)

> Relative humidity in percent (%) is the ratio of the quantity of water vapour the air contains compared to the maximum amount it can hold at that particular temperature.

### Precip. Amount (mm)

> Any and all forms of water, liquid or solid, that falls from clouds and reaches the ground. This includes drizzle, freezing drizzle, freezing rain, hail, ice crystals, ice pellets, rain, snow, snow pellets, and snow grains. Types of precipitation that originate aloft are classified under Liquid Precipitation, Freezing Precipitation and Frozen Precipitation. The measurement of precipitation is expressed in terms of vertical depth of water (or water equivalent in the case of solid forms) which reaches the ground during a stated period. The millimetre (mm) is the unit of measurement of liquid precipitation and the vertical depth of water or water equivalent is express to the nearest 0.2 mm.

### Stn Press (kPa)

> The atmospheric pressure in kilopascals (kPa) at the station elevation. Atmospheric pressure is the force per unit area exerted by the atmosphere as a consequence of the mass of air in a vertical column from the elevation of the observing station to the top of the atmosphere.


## Crash data

Crash data from insurance companies is generally more comprehensive than police data.

From the ICBC website:

> ICBC crash data is generally much larger in volume than police crash data because:
- Basic insurance coverage through ICBC is mandatory; therefore crash occurrences are reported to ICBC.
- Whereas, police do not attend all crashes. Typically only the more serious crashes involving injury or fatality
are attended. In addition, the number of reports submitted by individuals to police is very low, as it’s not
mandatory that a crash be reported to police.

![](./misc/ICBC_data_dictionary.png)


# Data Cleaning

## Weather data

<!-- add a variable for snow/rain by taking if precip. amount > 0 and if temp <= 0, then snow, otherwise rain -> not great, but no other indicator is present -->


## Crash Data



# Statistical Analysis

## Title 1
