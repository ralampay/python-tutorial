# Pandas Exercises

## Exercise 1: Production Data Analysis

### Dataset A: `production_data.csv`:

```
ProductID,ProductName,QuantityProduced,ProductionDate
1,Gadget A,150,2024-01-15
2,Gadget B,200,2024-01-20
3,Gadget C,300,2024-01-25
4,Gadget D,250,2024-01-30
5,Gadget E,100,2024-02-01
```

### Dataset B: `quality_control.csv`:

```
ProductID,ProductName,QualityScore,InspectionDate
1,Gadget A,85,2024-01-16
2,Gadget B,90,2024-01-21
3,Gadget C,75,2024-01-26
4,Gadget D,95,2024-01-31
5,Gadget E,80,2024-02-02
```

### Instructions

1. Load the two CSV files into separate DataFrames.

2. Use concat() to combine the two datasets into one DataFrame

3. Use merge() to join the two datasets on ProductID. Perform an outer join.

4. Create a new column called `ProductionQuality` based on the `QualityScore`. Use a custom function to classify scores:

* If the score is 85 or above, classify as "Good"
* If the score is between 70 and 85, classify as "Average"
* If the score is below 70, classify as "Poor"

## Exercise 2: Manufacturing Efficiency

### Dataset A: `machine_data.csv`

```
MachineID,MachineName,HoursOperated,MaintenanceDate
101,Machine A,120,2024-02-01
102,Machine B,150,2024-02-05
103,Machine C,90,2024-02-10
104,Machine D,180,2024-02-15
105,Machine E,110,2024-02-20
```

### Dataset B: `downtime_data.csv`

```
MachineID,MachineName,DowntimeHours,IssueDate
101,Machine A,5,2024-02-02
102,Machine B,2,2024-02-06
103,Machine C,3,2024-02-11
104,Machine D,0,2024-02-16
105,Machine E,4,2024-02-21
```

### Instructions

1. Load the two CSV files into separate DataFrames.

2. Use concat() to combine the two datasets into one DataFrame

3. Use merge() to join the two datasets on MachineID. Perform an outer join.

4. Create a new column called EfficiencyScore based on the HoursOperated and DowntimeHours. Use the formula:

```python
efficiency_score = ((hours_operated / downtime_hours) / hours_operated) * 100
```

5. Classify the scores:

* If the score is 90 or above, classify as "High Efficiency"
* If the score is between 70 and 90, classify as "Medium Efficiency"
* If the score is below 70, classify as "Low Efficiency"
