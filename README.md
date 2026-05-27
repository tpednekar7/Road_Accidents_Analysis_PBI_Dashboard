                                          Road Accident Analysis

🚦 Road Accident Analysis — Power BI Dashboard
A Power BI dashboard analyzing UK road accident data for 2021 and 2022, built to uncover patterns in casualty severity, vehicle involvement, road conditions, and geographic hotspots.

📊 Dashboard Overview
The dashboard is filtered globally by Road Surface Conditions and Weather Conditions dropdowns, affecting all visuals simultaneously.
KPI Cards
KPIDescriptionTotal CasualtiesTotal people injured or killed across all accidentsTotal AccidentsCount of unique accident recordsFatal CasualtiesAccidents with severity = FatalSerious CasualtiesAccidents with severity = SeriousSlight CasualtiesAccidents with severity = Slight
Each KPI shows a YoY % change vs the previous year.

📈 Visuals
VisualChart TypeField UsedCasualties by VehiclePictogram / Card ListVehicle_TypeCasualties by Month and YearArea ChartAccident DateCasualties by Urban/Rural AreaDonut ChartUrban_or_Rural_AreaCasualties by Road TypeHorizontal Bar ChartRoad_TypeCasualties by Light ConditionsDonut ChartLight_ConditionsCasualties by LocationMapLatitude / Longitude

🗂️ Dataset

Source: UK Police-reported road accident records
Years: 2021 – 2022
Granularity: One row per accident (Accident_Index is the primary key)

Key Columns
ColumnDescriptionAccident_IndexUnique accident ID (Primary Key)Accident_SeverityFatal / Serious / SlightNumber_of_CasualtiesTotal casualties per accidentVehicle_TypeCar, Bike, Bus, Van, Agricultural, etc.Road_TypeSingle carriageway, Dual, Roundabout, etc.Road_Surface_ConditionsDry, Wet or damp, Frost/Ice, etc.Light_ConditionsDaylight / DarkUrban_or_Rural_AreaUrban / RuralWeather_ConditionsFine, Rain, Snow, Fog, etc.Latitude / LongitudeCoordinates for map visual


1. Project Overview
This Power BI dashboard provides an end-to-end visual analysis of road accident data recorded across the United Kingdom for the years 2021 and 2022. The goal is to surface actionable insights about accident severity, contributing conditions, and geographic hotspots to support road safety decision-making.
The dashboard enables stakeholders to quickly understand where accidents are happening, under what conditions, and which vehicle types are most involved, while tracking year-over-year changes across all key metrics.

2. Data Source
Dataset
•	Source: UK road accident records (Police-reported data)
•	Years covered: 2021 and 2022
•	Granularity: One row per accident (unique Accident_Index)
•	Supporting table: Calendar Date table with Year, Month, Date columns

Dataset Columns

Column Name	Description
Accident_Index	Unique identifier for each accident record (Primary Key)
Accident Date	Date the accident occurred
Day_of_Week	Day of the week (e.g., Monday, Thursday)
Junction_Control	Type of traffic control at the junction
Junction_Detail	Nature of the junction (e.g., T-junction, Crossroads)
Accident_Severity	Severity level: Fatal, Serious, or Slight
Latitude / Longitude	Geographic coordinates for mapping accidents
Light_Conditions	Lighting at time of accident (Daylight / Dark)
Local_Authority_(District)	District where the accident occurred
Carriageway_Hazards	Any hazards present on the carriageway
Number_of_Casualties	Total casualties in the accident
Number_of_Vehicles	Number of vehicles involved
Police_Force	Police force that recorded the accident
Road_Surface_Conditions	Surface state: Dry, Wet or damp, etc.
Road_Type	Type of road: Single carriageway, Dual, Roundabout, etc.
Speed_limit	Posted speed limit at accident location
Time	Time of accident (HH:MM)
Urban_or_Rural_Area	Whether the accident was in Urban or Rural setting
Weather_Conditions	Weather at time of accident
Vehicle_Type	Type of vehicle involved (Car, Bike, Bus, Van, etc.)

3. Key Performance Indicators (KPIs)
The top section of the dashboard presents five headline KPI cards, each showing the current year value alongside a percentage change vs. the prior year (displayed in red to indicate decline or increase in severity).

KPI	Description
Total Casualties	Sum of all people injured or killed across all recorded accidents.
Total Accidents	Count of unique accident records (by Accident_Index).
Fatal Casualties	Accidents with Accident_Severity = Fatal.
Serious Casualties	Accidents with Accident_Severity = Serious.
Slight Casualties	Accidents with Accident_Severity = Slight.

Each KPI uses a Year-to-Date (YTD) DAX measure scoped to the selected year using DATESYTD with VALUES('Calendar'[Year]) to ensure correct year isolation when filtered via the year slicer.

4. Dashboard Visuals
The dashboard contains six visuals covering vehicle, temporal, geographic, and road condition dimensions of accident data.

Visual Name	Chart Type	Data Field	Key Insight
Casualties by Vehicle	Pictogram / Card List	Vehicle_Type	Breaks down casualties by vehicle category: Car, Bike, Bus, Van, Agricultural, Others.
Casualties by Month and Year	Area Chart	Accident Date	Shows monthly trend across 2021 and 2022, allowing YoY seasonal comparison.
Casualties by Urban/Rural Area	Donut Chart	Urban_or_Rural_Area	Compares the proportion of accidents in urban vs. rural settings.
Casualties by Road Type	Horizontal Bar Chart	Road_Type	Ranks road types (Single carriageway, Dual carriageway, Roundabout, etc.) by casualty count.
Casualties by Light Conditions	Donut Chart	Light_Conditions	Splits accidents between Daylight and Dark conditions.
Casualties by Location	Map Visual	Latitude / Longitude	Plots each accident geographically across the UK for spatial hotspot analysis.

5. Filters & Slicers
Two dropdown slicers are positioned in the top-right of the dashboard to allow cross-filtering of all visuals simultaneously:

Slicer	Source Field	Values
Road Surfaces	Road_Surface_Conditions	Dry, Wet or damp, Frost/Ice, Snow, Flood, etc.
Weather Conditions	Weather_Conditions	Fine no high winds, Rain, Snow, Fog, etc.

Tools & Technologies
•	Power BI Desktop - Dashboard development, DAX measures, visuals
•	Microsoft Bing Maps / ArcGIS - Geographical casualty mapping
•	Power Query (M) - Data transformation and Calendar table generation
•	DAX - KPI calculations, YTD measures, YoY comparisons

