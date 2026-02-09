# NYC Taxi Analytics (2013) — Pure Python (No PySpark)

## Overview
I analyzed the NYC Taxi dataset using standard Python to answer three analytical questions related to taxi activity, driver performance, and profitability across different times of the day. The dataset was processed line by line to handle its size efficiently, and basic data cleaning was applied by skipping malformed rows, header entries, and invalid records.
First, I identified the top 10 most active taxis by counting the number of unique drivers associated with each taxi. Next, I determined the top 10 best drivers based on their average earnings per minute by aggregating total earnings and total trip time for each driver. Finally, I analyzed profitability across different hours of the day by computing the ratio of total surcharge to total travel distance for each hour and identifying the most profitable hour to work.
For each task, execution time was measured to evaluate performance. The results show realistic real-world patterns, such as higher profitability during evening hours, and demonstrate that efficient data processing and simple data structures can effectively analyze large datasets.
## Dataset
Each row is a taxi trip record with fields such as:
- taxi ID (medallion), driver ID (hack_license)
- pickup/dropoff time
- trip duration, distance
- surcharge, total amount
---

### Tasks Implemented

#### Task 1 — Top-10 Active Taxis
Identified the top 10 taxis that had the highest number of unique drivers by mapping taxi IDs to sets of driver IDs and ranking them by count.

#### Task 2 — Top-10 Best Drivers
Computed the top 10 drivers based on money earned per minute by aggregating total earnings and total trip time across all valid trips.

#### Task 3 — Best Hour to Work
Determined the most profitable hour of the day by calculating the ratio of total surcharge earned to total distance traveled for each hour using pickup time.

---

### Key Insights
- Taxi activity and driver earnings are highly unevenly distributed
- A small subset of drivers earns significantly more per minute
- Evening hours (around 7 PM) are the most profitable due to higher surcharges
- Simple Python data structures are sufficient for analyzing large datasets efficiently

---

### Performance
Each task reports execution time, demonstrating that sequential file processing with basic data cleaning scales well for moderately large datasets.

---

### Technologies Used
- Python
- Jupyter Notebook
- CSV file processing
- Dictionaries and sets
- Basic performance benchmarking

- ### Final Observations

The analysis reveals meaningful real-world trends in the NYC taxi dataset.  
A small number of taxis and drivers dominate activity, and evening hours show higher profitability due to increased surcharges.  
Overall, the tasks demonstrate that large datasets can be efficiently analyzed using simple Python data structures when combined with careful data cleaning and performance measurement.


### Task 1: Top-10 Active Taxis

In this task, the objective is to find the top 10 taxis that have been associated with the highest number of unique drivers.  
Each taxi is mapped to a set of drivers so that duplicate drivers are not counted multiple times.  
After processing the dataset, taxis are ranked based on the number of distinct drivers, and the top 10 are reported.  
The execution time is measured to evaluate performance.

### Task 2: Top-10 Best Drivers

This task identifies the top 10 drivers based on money earned per minute.  
For each driver, the total amount earned and the total trip time are accumulated across all valid trips.  
The earning rate is computed as total earnings divided by total trip time in minutes.  
Drivers are then ranked by this rate to determine the top performers, and the processing time is recorded.

### Task 3: Best Time of the Day to Work

In this task, the goal is to determine which hour of the day is the most profitable for taxi drivers.  
Profitability is defined as the ratio of total surcharge earned to total trip distance traveled for each hour of the day.  
The pickup time is used to group trips by hour, and rows with invalid distance values are skipped.  
The hour with the highest profit ratio is reported as the best time to work, along with the execution time.

