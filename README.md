# Airport Performance Analysis - Power BI Dashboard
![Logo](https://github.com/Aya-Mohamedd/Airline-Flights-Delay/blob/main/Screenshots/Logo.png)

## 1. Problem Overview
Flight delays, cancellations, and diversions are major concerns in the airline industry, affecting customer satisfaction, operational efficiency, and revenue. This Power BI dashboard analyzes airport performance based on flight data to identify key trends and problem areas.
<hr>

## 2. Project Overview
This project involves importing, transforming, modeling, and visualizing flight performance data using Power BI. The dashboard consists of multiple pages focusing on various aspects of flight operations, including delays, cancellations, and airline performance metrics.
<hr>


## 3. Database Description
The dataset includes information on:
- **Flight schedules which includes** :
  
    **ID** –Id of the flight.

    **Year** – The year in which the flight took place.

    **Month** – The month of the flight (1 = January, 12 = December).

    **DayofMonth** – The day of the month when the flight occurred.

    **DayOfWeek** – The day of the week (1 = Monday, 7 = Sunday).

   **DepTime** – The actual departure time of the flight (in HHMM format, e.g., 1530 means 3:30 PM).

    **CRSDepTime** – The scheduled departure time according to the Computerized Reservation System (CRS), also in HHMM format.

    **ArrTime** – The actual arrival time of the flight (in HHMM format).

    **CRSArrTime** – The scheduled arrival time according to CRS.

   **UniqueCarrier** – The airline code or identifier for the carrier operating the flight.

    **FlightNum** – The flight number assigned by the airline.

    **TailNum** – The aircraft’s tail number (a unique identifier for the plane).

    **ActualElapsedTime** – The total actual time (in minutes) from departure to arrival.

    **CRSElapsedTime** – The scheduled elapsed time (in minutes) from departure to arrival.

    **AirTime** – The actual time (in minutes) the aircraft spent in the air.

    **ArrDelay** – The difference (in minutes) between the actual and scheduled arrival times (positive values indicate a delay).

    **DepDelay** – The difference (in minutes) between the actual and scheduled departure times (positive values indicate a delay).

    **Origin** – The origin airport code (e.g., LAX for Los Angeles International Airport).

    **Dest** – The destination airport code.

    **Distance** – The flight distance between the origin and destination (in miles).

    **TaxiIn** – The time (in minutes) the aircraft spent taxiing after landing.

    **TaxiOut** – The time (in minutes) the aircraft spent taxiing before takeoff.

    **Cancelled** – Indicates whether the flight was canceled (1 = Yes, 0 = No).

    **CancellationCode** – The reason for flight cancellation:

    "A" = Carrier (airline) cancellation
    "B" = Weather-related cancellation
    "C" = National Air System (NAS) delay
    "D" = Security-related cancellation
    Diverted – Indicates whether the flight was diverted (1 = Yes, 0 = No).

    **CarrierDelay** – The delay (in minutes) due to the airline (e.g., maintenance, crew issues).

    **WeatherDelay** – The delay (in minutes) due to weather conditions.

    **NASDelay** – The delay (in minutes) caused by National Airspace System (e.g., air traffic control, capacity constraints).

    **SecurityDelay** – The delay (in minutes) due to security-related issues.

    **LateAircraftDelay** – The delay (in minutes) caused by a previous flight arriving late and affecting the aircraft’s schedule.
<hr>


## 4. Tools and Technologies Used
- **Power BI**: For data visualization and reporting
- **DAX (Data Analysis Expressions)**: For creating calculated measures
- **Power Query**: For data transformation and cleansing
<hr>


## 5. Data Model
![Model](https://github.com/Aya-Mohamedd/Airline-Flights-Delay/blob/main/Screenshots/Model.png)

The data model consists of:
- **Fact Tables**:
  - Delayed Flights
- **Dimension Tables**:
  - Airport Codes
  - Carrier
  - Time dimension
  - Date dimention



Relationships are established between fact and dimension tables to enable cross-analysis.
<hr>


## 6. Analysis Process/Methodology
1. **Data Preparation & Cleaning**
   - Importing the dataset into Power BI
   - Removing duplicates and handling missing values by replacing it with zeros in delay reasons columns and adding extra column called UnknownReasonDelay 
   - Creating relationships between tables   
2. **Data Modeling**
   - Developing calculated columns and measures using DAX
   - Creating hierarchies and groupings
3. **Visualization Development**
   - Building interactive dashboards with charts, tables, and KPIs
   - Implementing drill-through features for deeper insights
<hr>


## 7. Key Visualizations & Insights
### **1. Cover Page**
![0-Cover](https://github.com/Aya-Mohamedd/Airline-Flights-Delay/blob/main/Screenshots/0-Cover.png)
- Provides quick navigation and AI-powered Q&A for data insight<br>

### **2. Overview Dashboard**
![1-Overview](https://github.com/Aya-Mohamedd/Airline-Flights-Delay/blob/main/Screenshots/1-Overview.png)
- KPIs: 2M total flights, 5367 aircrafts, 304 active airports
- Bar chart: Top 10 delayed airports (Houston highest)
- Line chart: Flights trend shows peaks in winter
- Pie chart: NAS and Late Aircraft delays dominate
- Carriers: JetBlue and Comair show highest average delays<br>


### **3. Flights Dashboard**
![2-Flights](https://github.com/Aya-Mohamedd/Airline-Flights-Delay/blob/main/Screenshots/2-Flights.png)
- 27K on-time, 633 canceled, 7754 diverted flights
- Top 10 cancellations: Pinnacle & Mesa Airlines
- Southwest leads in total flights
- Evening has highest average taxi-out time


### **4. Delay Dashboard**
![3-Delays](https://github.com/Aya-Mohamedd/Airline-Flights-Delay/blob/main/Screenshots/3-Delays.png)
- Delay type KPIs: Late Aircraft (25.30 mins), NAS (15.02), Weather (3.70)
- Cancellations peak on Tuesdays
- JetBlue and Comair show high delays again


### **5. Airport Dashboard**
![4-Airport](https://github.com/Aya-Mohamedd/Airline-Flights-Delay/blob/main/Screenshots/4-Airport.png)
- ATL and ORD lead in flights
- Merle K. and Yakutat: Highest delay percentages
- Midway has top cancellation rate


### **6. Geographic Insights**
![5-Map](https://github.com/Aya-Mohamedd/Airline-Flights-Delay/blob/main/Screenshots/5-Map.png)
- Regional stats show 19K flights in Texas, but only 206 on-time
- High delays in central U.S.


### **7. Tooltip Summary Cards**
![6-Tooltip](https://github.com/Aya-Mohamedd/Airline-Flights-Delay/blob/main/Screenshots/6-Tooltip.png)
- Fast insights: Total, On-Time, Delayed Flights + Delay times
- Canceled Flights: 633
- Departure Delay: 43.19 mins | Arrival Delay: 42.20 mins

## I welcome feedback, suggestions, and contributions to improve this project! Feel free to reach out or collaborate to make it even better
