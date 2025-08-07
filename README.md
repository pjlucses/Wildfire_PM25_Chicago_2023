# Wildfire_PM25_Chicago_2023
Processed dataset of indoor and outdoor daily average PM2.5 concentrations from PurpleAir sensors in the Chicago area, 2023. The dataset also includes daily smoke category classifications (none, light, medium, heavy) and community identifiers for each sensor pair.
# Processed Dataset: Indoor and Outdoor Daily Average PM2.5 Concentrations – Chicago Area, 2023

## Description
This dataset contains **daily average PM2.5 concentrations** measured by indoors and outdoors by PurpleAir sensors in the Chicago area during 2023. The dataset has been processed from raw 2-minute PurpleAir measurements according to the correction equations described in **Barkjohn et al. (2021)** and aggregated to daily averages.

The dataset includes:
- **smoke** Daily smoke category classifications (none, light, medium, heavy) based on NOAA’s Hazard Mapping System (HMS) smoke data.
- **sensor_index** PurpleAir sensor index number
- **location_typle** indicates the sensor type: =1 means indoor; =0 means outdoor
- **community** community name, corresponding to the eight communities analyzed in the study.
- **latitude** latitude of the sensor
- **longitude.x** longitude of the sensor
- **daily_PM25** corrected daily average PM2.5 concentration 
- **daily_RH** daily average relative humidity

  
This dataset supports the reproducibility of analyses presented in:  
> Jing, P., Whalen, M., & Hartnett, N. (2025). *Indoor Air Quality Response to Wildfire Smoke: A Case Study in Chicago Using PurpleAir Sensors.*

---

## File Information
- **File name:** `DailyPM25_Chicago_2023_processed.csv`  
- **Format:** CSV (comma-separated values)  

---

## Variables
| Column Name         | Description |
|---------------------|-------------|
| `date`              | Date of measurement (MM/DD/YY) |
| `community`         | Community name (e.g., Far North Side, West Ridge, Edgewater, North Park, Irving Park, Near North Side, The Loop, Near South Side) |
| `sensor_id`         | PurpleAir sensor ID |
| `location_type`     | Location of the sensor: 0 means outdoor sensor; 1 means indoor sensor |
| `daily_pm25`        | Daily average PM2.5 concentration (µg m^-3, corrected) |
| `smoke`             | Daily smoke classification: none, light, medium, heavy |
| `daily_RH`          | Daily relative humidity (%) |
| `latitude`          | Latitude of the PurpleAir sensor |
| `longitude`         | Longitude of the PurpleAir sensor |

---

## Methods Summary
1. **Raw data acquisition:** Downloaded raw 2-minute PM2.5 data from [PurpleAir](https://www2.purpleair.com/) for 18 indoor and 68 outdoor sensors in the Chicago area.  
2. **Sensor pairing:** Selected 10 indoor sensors with ≥4 months of continuous observations in 2023, paired each with the nearest outdoor sensor within 1 km.  
3. **Data correction:** Applied **Barkjohn et al. (2021)** U.S.-wide correction equations for PurpleAir sensors, accounting for relative humidity.  
4. **Daily averaging:** Aggregated corrected 2-minute measurements to daily averages for each sensor.  
5. **Smoke classification:** Merged with NOAA HMS daily smoke shapefiles for 2023; assigned smoke category based on the highest density observed over Chicago.

---

## License
This dataset is licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.  
You are free to share and adapt the material for any purpose, provided appropriate credit is given.  
[Read the license here](https://creativecommons.org/licenses/by/4.0/).

---

## Citation
If you use this dataset, please cite both the dataset and the associated publication:

**Dataset citation:**  
Jing, P., Whalen, M., & Hartnett, N. (2025). *Processed dataset of paired indoor and outdoor daily average PM₂.₅ concentrations from PurpleAir sensors in the Chicago area, 2023*. [GitHub/Zenodo link].

**Publication citation:**  
Jing, P., Whalen, M., & Hartnett, N. (2025). *Indoor Air Quality Response to Wildfire Smoke: A Case Study in Chicago Using PurpleAir Sensors.* [Journal Name], [Volume(Issue)], [Page numbers]. https://doi.org/[DOI]

---

## Contact
For questions or additional information, please contact:  
**Ping Jing**  
School of Environmental Sustainability  
Loyola University Chicago  
📧 [pjing@luc.edu](mailto:pjing@luc.edu)
