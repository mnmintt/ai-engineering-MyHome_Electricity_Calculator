## 1. Dataset Information

| Item | Description |
|---|---|
| Dataset Name | Monthly Electricity Consumption |
| Data Source | OpenDOSM |
| File Name | electricity_consumption.csv |
| File Format | CSV |
| Number of Rows | 612 |
| Number of Columns | 3 |
| Data Type | Tabular Data |

## 2. Dataset Structure

| Column | Description |
|---|---|
| date | Monthly record date |
| sector | Electricity consumption sector |
| consumption | Electricity consumption value in MKWh |

## 3. Initial Data Inspection

The dataset was loaded successfully using Python and pandas in Google Colab.

Inspection results:

- Total rows: 612
- Total columns: 3
- Missing values: 0
- Duplicate rows: 0

## 4. Initial Observations

- The dataset contains monthly electricity consumption records.
- The dataset includes date, sector, and consumption information.
- No missing values were found.
- No duplicate rows were found.
- The dataset can be used for general electricity consumption analysis.

## 5. Limitations

- The dataset represents electricity consumption by sector, not individual households.
- It does not contain appliance wattage or daily usage hours.
- It cannot directly calculate an individual household's electricity bill.
- Tariff information must come from a separate source.

## 6. Data Preparation Decision

Since the dataset contains no missing values or duplicate rows, removing records is not necessary. Further preparation will focus on checking the date format, data types, and validity of consumption values.
