## 1. Data Source Selection

The project uses the electricity consumption dataset from OpenDOSM.

**Source:** https://open.dosm.gov.my/data-catalogue/electricity_consumption

The dataset was selected because it provides official electricity consumption records in Malaysia. It contains 612 rows and 3 columns: `date`, `sector`, and `consumption`.

This dataset is suitable for understanding general electricity consumption patterns across different sectors.

## 2. Data Preparation Decisions

The CSV pathway was selected because the source dataset is structured in tabular format.

The following preparation steps were performed:

- Converted the `date` column from text into datetime format.
- Checked for missing values.
- Checked for duplicate rows.
- Checked for invalid dates.
- Checked for negative consumption values.
- Exported the prepared dataset as `electricity_consumption_cleaned.csv`.

No rows needed to be removed because the dataset passed the validation checks.

## 3. Data Validation Results

| Validation | Result |
|---|---:|
| Total rows | 612 |
| Missing values | 0 |
| Duplicate rows | 0 |
| Invalid dates | 0 |
| Negative consumption values | 0 |
| Required columns available | Yes |

All validation checks passed successfully.

## 4. ETL or ELT Decision

The project uses the ETL approach.

- **Extract:** Load the original electricity consumption CSV from the source.
- **Transform:** Convert the date column and perform data validation.
- **Load:** Export the prepared dataset as a new CSV file.

ETL was selected because the dataset is prepared before being saved for later use.

## 5. Batch or Streaming Decision

Batch processing was selected because the OpenDOSM dataset contains historical monthly electricity consumption records.

The system does not require real-time electricity readings or continuous data updates. Therefore, batch processing is sufficient for the current project.

## 6. Data Limitations

The dataset provides sector-level electricity consumption rather than individual household appliance usage.

Therefore, it cannot directly determine the electricity consumption of a specific household, room, or appliance.

The Home Energy Calculator will use user-provided appliance information for its calculations. The OpenDOSM dataset will be used as a reference for general electricity consumption patterns.

## 7. Pipeline Output

The pipeline produces the following files:

- `electricity_consumption_cleaned.csv` – Prepared electricity consumption dataset.
- `week3_manifest.json` – Records the source information, output information, preparation steps, and validation results.
- `pipeline_manifest.json` – Records the pipeline execution and provenance information.

The prepared dataset is stored in the project's `data/processed/` directory, while the V1 pipeline outputs are stored in `data/pipeline_v1/`.

## 8. Repeatability and Provenance

A repeatability test was performed by executing the pipeline twice.

Both executions produced the same SHA-256 hash:

`7663e8045981ab53cbdae7520a29389b060c13bfe5c2d56a964d7a397052edca`

The test results were:

- Same output file: True
- Consumption values preserved: True

This confirms that the pipeline produces consistent output when executed again.

The lineage manifest also records the source and output SHA-256 hashes to help track the dataset's origin and prepared version.

## 9. Conclusion

The CSV data pipeline was successfully implemented and validated. The original dataset was prepared, checked, and exported into a cleaned CSV file.

The pipeline is repeatable and records its data lineage. The prepared dataset can be used as a reference for the next stages of the MyHome Energy Calculator project.
