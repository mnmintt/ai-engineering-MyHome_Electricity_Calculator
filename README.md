# MyHome Electricity Calculator

> An AI-powered household energy management system that helps Malaysian households understand electricity consumption, estimate electricity costs, and receive personalised energy-saving recommendations through an AI assistant and chatbot

## Problem Statement
Many households do not know which rooms and appliances consume the most electricity or how their daily habits affect their electricity bills. Existing calculators can estimate energy usage, but users may need more personalised guidance to understand their results and identify possible improvements. MyHome Energy Calculator combines electricity calculations, bill calculators,  interactive dashboards, AI recommendations, a chatbot, and a what-if simulator to help users make better energy-saving decisions.

## Evidence of the Problem
 - **Evidence 1:** Tenaga Nasional Berhad (TNB) provides household energy calculation tools and energy-saving guidance. This provides a starting point for understanding existing solutions and identifying opportunities for improvement.
   (Source: https://www.tnb.com.my/residential/energy-savings-at-home)
- **Evidence 2:** Household electricity costs depend on factors such as appliance power ratings, usage hours, and applicable electricity tariffs. The Energy Commission also explains the components of the electricity pricing framework.
  (Source: https://www.tnb.com.my/residential/energy-savings-at-home#usage-cost-of-electrical-appliances-at-home)
  
## Initial Related Work / Existing Approaches
**1. TNB Home Energy Calculator**
- Allows users to configure a household and estimate electricity usage through household and appliance information.
- Source: https://hec.tnb.com.my/Public/UsageCalculator
  
**2. Energy Commission Electricity Pricing Framework**
- Explains electricity tariff components and the pricing framework in Peninsular Malaysia.
- Source: https://www.st.gov.my/pricing/electricity-pricing-framework/components-ibr#section-2

**3. TNB Bill Calculator**
- Allow users to calculate estimated bill based on tariff type
- Source: https://www.mytnb.com.my/tariff/index.html?lang=en&v=1.1.70#calculator 

## Project Objectives
- O1: To develop estimated bill calculator and an interactive household energy calculator that estimates electricity consumption where costs based on rooms, appliances, and usage patterns.
- O2: To develop a dashboard that compares electricity consumption across floors, rooms, and appliances.
- O3: To implement AI-powered recommendations, a chatbot, and a what-if simulator to help users understand their energy usage and explore potential savings.
  
## Target Users
- Malaysian households that want to understand their electricity consumption.
- Homeowners and tenants who want to identify appliances that use more electricity.
- Users who want to explore ways to reduce electricity usage and estimated bills.
  
## Data Sources
- **Source 1:** OpenDOSM Monthly  Electricity Consumption Dataset (Monthly Consumption) - https://open.dosm.gov.my/data-catalogue/electricity_consumption?sector=total&visual=table
- **Source 2:** Energy Commission Electricity Pricing Framework - https://www.st.gov.my/pricing/electricity-pricing-framework/components-ibr
- **Source 3:** TNB Energy Savings at Home (Saving recommendation)  - https://www.tnb.com.my/residential/energy-savings-at-home#usage-cost-of-electrical-appliances-at-home
- **Source 4:** Electricity Pricing Framework (Tariff) - https://myenergystats.st.gov.my/en/dashboard  
  
## Weekly Progress

| Week | Focus | Deliverable | Status |
|------|-------|-------------|--------|
| W1 | System map + project scope | README + project scope + observation sheet + system map | ✅ Completed |
| W2 | Requirements + system design | Functional and non-functional requirements + architecture + ADR | ✅ Completed |
| W3 | Data engineering: pipeline, lineage and workflows | Pipeline notebook + data inventory + pipeline diagram + pipeline decisions + cleaned dataset + manifests + V1 pipeline | ✅ Completed |
