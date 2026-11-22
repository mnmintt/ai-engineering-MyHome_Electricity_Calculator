

## Section 1 — Functional Requirements

| ID | Requirement — The system SHALL | Scope Boundary — SHALL NOT (where relevant) |
|---|---|---|
| FR1 | Allow users to configure their household type, number of floors, rooms, and household structure for the Home Energy Calculator. | SHALL NOT require users to configure a household to use the Estimated Bill Calculator. |
| FR2 | Allow users to enter appliance names, quantities, wattage, and daily usage hours for the Home Energy Calculator. | SHALL NOT assume that missing or unknown appliance information is accurate. |
| FR3 | Calculate estimated daily and monthly electricity consumption for the Home Energy Calculator using appliance wattage, quantity, and usage duration. | SHALL NOT use AI-generated values as a replacement for the calculation formula. |
| FR4 |Display estimated electricity consumption statistics by appliance, room and wattage in the Home Energy Calculator. | SHALL NOT display statistics that cannot be calculated from the available input data. |
| FR5 | Allow users to select a tariff type and enter the required billing information in the Estimated Bill Calculator, then calculate an estimated electricity bill using documented tariff rates and assumptions. | SHALL NOT require room or appliance configuration, or claim that the result is the exact TNB bill. |
| FR6 | Generate AI-based energy-saving recommendations and answer household energy questions using available household data and relevant energy-saving information in the Home Energy Calculator. | SHALL NOT present unsupported assumptions as confirmed household facts or require users to use the Estimated Bill Calculator first. |
| FR7 | Allow users to change appliance usage assumptions and compare estimated electricity consumption before and after the changes in the Home Energy Calculator. | SHALL NOT claim that simulated savings are guaranteed real-world savings. |
| FR8 | Allow users to view national and sector-level electricity consumption trends using available electricity consumption data. | SHALL NOT present national or sector-level data as individual household electricity consumption. |

---

## Section 2 — Non-Functional Requirements

| ID | Quality Attribute | Requirement | Measurement Method | Metric | Threshold |
|---|---|---|---|---|---|
| NFR1 | Correctness | The system shall calculate electricity consumption accurately using the defined formula in the Home Energy Calculator. | Compare results against manually calculated test cases covering different wattages, quantities, and usage hours. | Absolute calculation error in kWh | ≤ 0.01 kWh for predefined test cases |
| NFR2 | Performance | The system shall return local calculations and dashboard updates within an acceptable time for both calculators. | Measure response time across a defined set of bill calculations, energy calculations, and dashboard operations. | 90th-percentile response time (p90) | ≤ 3 seconds for local operations |
| NFR3 | Reliability | The system shall complete valid bill and energy calculation requests without calculation errors. | Run at least 50 valid test cases covering both calculators and record successful completions. | Successful calculation rate | 100% of valid test cases |
| NFR4 | Usability | Users shall be able to complete the basic tasks of each calculator without assistance. | Conduct a usability test with five intended users who independently try the Estimated Bill Calculator and Home Energy Calculator. | Number of users completing the defined tasks without assistance | At least 4 out of 5 users |

---

## Section 3 — Responsible AI Requirements

| ID | Responsible AI Risk | Requirement | Measurement Method | Metric | Threshold |
|---|---|---|---|---|---|
| RAI1 | Recommendation Quality | The system shall provide relevant and practical energy-saving recommendations based on available household data in the Home Energy Calculator. | Evaluate 20 recommendations using a predefined rubric for relevance, practicality, and consistency with supplied data. | Recommendations meeting the rubric | At least 18 out of 20 |
| RAI2 | Transparency and Missing Data | The system shall acknowledge missing or insufficient information and identify when an estimate depends on assumptions in either calculator. | Test cases with missing appliance data, billing inputs, or tariff information. | Test cases that correctly acknowledge missing information | 100% of defined missing-data test cases |
| RAI3 | Privacy | The system shall avoid sending unnecessary personal identifiers to an external AI service used by the Home Energy Calculator. | Inspect outgoing AI requests using test household profiles. | Requests containing unnecessary direct personal identifiers | 0 in the defined test cases |
| RAI4 | Numerical Grounding | AI-generated responses in the Home Energy Calculator shall use verified energy calculation results for electricity consumption and cost figures, or clearly identify when a value is an unavailable estimate. | Compare chatbot responses against calculation-engine outputs using a predefined test set. | Numerical claims matching verified results or correctly labelled as unavailable estimates | 100% of tested numerical claims |
