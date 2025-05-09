
# Airport Performance Analysis - Power BI Dashboard

## 1. Problem Overview
Flight delays, cancellations, and diversions are major concerns in the airline industry, affecting customer satisfaction, operational efficiency, and revenue. This Power BI dashboard analyzes airport performance based on flight data to identify key trends and problem areas.

---

## 2. Project Overview
This project involves importing, transforming, modeling, and visualizing flight performance data using Power BI. The dashboard consists of multiple pages focusing on various aspects of flight operations, including delays, cancellations, and airline performance metrics.

---

## 3. Database Description

The dataset includes information on:

- Flight schedules including:
  - Flight ID, Year, Month, Day of Month/Week
  - Departure/Arrival times (scheduled and actual)
  - Carrier and flight numbers
  - Aircraft tail numbers and elapsed times
  - Delay reasons: Carrier, Weather, NAS, Security, Late Aircraft
  - Flight origin and destination
  - Cancellation and diversion flags
  - Distance, Taxi In/Out times

---

## 4. Tools and Technologies Used
- **Power BI**: For data visualization and reporting
- **DAX (Data Analysis Expressions)**: For creating calculated measures
- **Power Query**: For data transformation and cleansing

---

## 5. Updated Data Model

The enhanced data model includes:

- **Fact Table**:
  - `DelayedFlights`: Flight details, delays, distances, and KPIs

- **Dimension Tables**:
  - `Carrier`: Carrier names with IATA/ICAO codes
  - `airport-codes.csv`: Airport and location details
  - `DimDate`: Date hierarchies (Year, Quarter, Month, Day)
  - `DimTime`: Time dimensions (Hour, Time of Day)

### Relationships:
- `DelayedFlights[DateKey]` → `DimDate[DateKey]`
- `DelayedFlights[TimeKey]` → `DimTime[TimeKey]`
- `DelayedFlights[Carrier Name]` → `Carrier[Carrier Name]`
- `DelayedFlights[Dest]` → `airport-codes.csv[iata]`

---

## 6. Analysis Process/Methodology

1. **Data Preparation & Cleaning**:
   - Imported data into Power BI
   - Handled nulls with defaults and added `UnknownReasonDelay`
   - Built structured relationships

2. **Data Modeling**:
   - Created DAX measures and hierarchies

3. **Visualization**:
   - Built interactive dashboards with tooltips, slicers, and KPIs

---

## 7. Key Visualizations & Insights

### 1. Cover Page
- Provides quick navigation and AI-powered Q&A for data insights

### 2. Overview Dashboard
- KPIs: 2M total flights, 5367 aircrafts, 304 active airports
- Bar chart: Top 10 delayed airports (Houston highest)
- Line chart: Flights trend shows peaks in winter
- Pie chart: NAS and Late Aircraft delays dominate
- Carriers: JetBlue and Comair show highest average delays

### 3. Flights Dashboard
- 27K on-time, 633 canceled, 7754 diverted flights
- Top 10 cancellations: Pinnacle & Mesa Airlines
- Southwest leads in total flights
- Evening has highest average taxi-out time

### 4. Delay Dashboard
- Delay type KPIs: Late Aircraft (25.30 mins), NAS (15.02), Weather (3.70)
- Cancellations peak on Tuesdays
- JetBlue and Comair show high delays again

### 5. Airport Dashboard
- ATL and ORD lead in flights
- Merle K. and Yakutat: Highest delay percentages
- Midway has top cancellation rate

### 6. Geographic Insights
- Regional stats show 19K flights in Texas, but only 206 on-time
- High delays in central U.S.

### 7. Tooltip Summary Cards
- Fast insights: Total, On-Time, Delayed Flights + Delay times
- Canceled Flights: 633
- Departure Delay: 43.19 mins | Arrival Delay: 42.20 mins

---

