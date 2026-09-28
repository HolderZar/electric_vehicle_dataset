# electric_vehicle_dataset
Analyzed a small public electric vehicle dataset using Google BigQuery and SQL.

## Tools
- Google BigQuery
- SQL
- Kaggle

## Questions
1. Which car has the fastest 0–100 km/h acceleration?
 
Select
Brand,
Model,
AccelSec

From `project-3d2c4d59-1d15-48e0-974.electric_vehicle_project.electric_cars`

order by AccelSec ASC

limit 1;

2. Which car has the highest efficiency?
   
SELECT
Brand,
Model,
Efficiency_WhKm

From `project-3d2c4d59-1d15-48e0-974.electric_vehicle_project.electric_cars`

order by Efficiency_WhKm ASC

Limit 1;

3. Does powertrain type relate to range, top speed, and efficiency?

SELECT
PowerTrain,
AVG(Range_km) as range_km,
AVG(topspeed_kmh) as topspeed_kmh,
AVG(Efficiency_Whkm) as efficiency_WhKm

From `project-3d2c4d59-1d15-48e0-974.electric_vehicle_project.electric_cars`

Group by PowerTrain;

4. Which manufacturer has the most vehicles?

Select 
Brand,
Count(*) as vehicle_count

from `project-3d2c4d59-1d15-48e0-974.electric_vehicle_project.electric_cars`

group by Brand

order by vehicle_count DESC

limit 1;

## Key Findings
- Tesla Roadster had the fastest acceleration at 2.1 seconds.
- Lightyear One had the best efficiency at 104 Wh/km.
- AWD vehicles had the highest average range and top speed, while FWD vehicles had the lowest Wh/km.
- Tesla had the highest amount of vehicles in the dataset, at 13. 

<img width="800" height="368" alt="65858f37-eab6-4ece-9b89-cae9b08faeca" src="https://github.com/user-attachments/assets/56b4dd02-6d0c-43f3-8960-e07524f9380b" />

<img width="800" height="360" alt="ede9ee40-df72-415f-bb0c-bca5f83aaacf" src="https://github.com/user-attachments/assets/81358b95-32ea-4b1d-9fc2-2e7da4fb2c1c" />

<img width="800" height="359" alt="b58ddf55-a756-4487-8231-8a47f1b2a87e" src="https://github.com/user-attachments/assets/54fab638-81b8-4e7b-bb6f-ef314f6934f7" />

<img width="800" height="361" alt="93fb5356-c2c4-4b27-b532-03bcaa089db5" src="https://github.com/user-attachments/assets/fe758f7b-ca9e-4205-a88d-121e3f11c5a1" />
<img width="1916" height="859" alt="image" src="https://github.com/user-attachments/assets/8f83484d-5d6e-45e7-893d-41f97819e17d" />

<img width="800" height="382" alt="07a12cf6-8243-4a5e-8da5-0fc8ef591b80" src="https://github.com/user-attachments/assets/e98ed841-ab8a-4686-9b88-c89a5f0cb957" />

## SQL Skills Used
- SELECT
- ORDER BY
- LIMIT
- AVG
- COUNT
- GROUP BY
- Aliases with AS

## What I Learned
- Lower AccelSec means faster acceleration.
- Lower Wh/km means better efficiency.
- GROUP BY lets me compare categories instead of individual rows.
- AVG and COUNT help summarize data.
- Semicolons separate SQL statements.
- Missing commas can cause syntax errors.
- WHERE was not used in this project, but I learned that it is used to filter rows based on specific conditions. For example, WHERE Range_Km > 400 would return only vehicles with a range greater than 400 km.
