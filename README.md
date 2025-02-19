Here’s a revised and improved version of your GitHub README. It’s more concise, better structured, and easier to read while retaining all the necessary information:

---

# US Natural Disaster Declarations: Basic EDA and Visualization

This repository contains a county-level dataset from the Federal Emergency Management Agency (FEMA) covering natural disaster declarations in the United States from **1953 to the present**. The dataset provides a high-level summary of federally declared disasters, including details about disaster types, affected areas, and aid programs triggered.

---

## About the Dataset

### Context
The United States experiences a wide range of natural disasters annually, including hurricanes, tornadoes, wildfires, and more. These events endanger lives and cause significant economic damage. FEMA plays a critical role in coordinating disaster response and providing relief funds to affected areas.

This dataset summarizes all federally declared disasters since 1953. It has been cleaned and formatted for ease of use, making it suitable for exploratory data analysis (EDA) and visualization.

---

### Content
The dataset includes two main files:

1. **`us_disaster_declarations.csv`**:  
   - Contains the full dataset with all rows and columns.  
   - Geographical resolution is at the county level, using FIPS codes to identify counties.  
   - Includes disaster types, timing features, and binary flags indicating whether specific aid programs were triggered.  

2. **`us_disasters_m5.csv`**:  
   - A subset of the data filtered for three states: California (CA), Texas (TX), and Wisconsin (WI).  
   - Designed for specific analysis constraints (e.g., disasters must have begun before May 23, 2016, and ended on or after January 29, 2011).  

---

### Column Descriptions
Below are the key columns in the dataset. Descriptions are adapted from FEMA's documentation, with additional clarifications where necessary.

#### Full Dataset (`us_disaster_declarations.csv`):
- **`fema_declaration_string`**: Unique identifier for Stafford Act declarations (concatenation of `declaration_type`, `disaster_number`, and `state`).  
- **`disaster_number`**: Sequentially assigned number for each disaster.  
- **`state`**: US state, district, or territory.  
- **`declaration_type`**: Type of declaration: "DR" (Major Disaster), "EM" (Emergency Management), or "FM" (Fire Management).  
- **`declaration_date`**: Date the disaster was declared.  
- **`fy_declared`**: Fiscal year of the declaration.  
- **`incident_type`**: Type of incident (e.g., "Fire", "Flood", "Hurricane").  
- **`declaration_title`**: Title of the disaster (e.g., "Hurricane Katrina", "Covid-19 Pandemic").  
- **`ih_program_declared`**: Binary flag for the "Individuals and Households Program".  
- **`ia_program_declared`**: Binary flag for the "Individual Assistance Program".  
- **`pa_program_declared`**: Binary flag for the "Public Assistance Program".  
- **`hm_program_declared`**: Binary flag for the "Hazard Mitigation Program".  
- **`incident_begin_date`**: Start date of the incident.  
- **`incident_end_date`**: End date of the incident (14% NA entries).  
- **`disaster_closeout_date`**: Date all financial transactions were completed (98% NA entries).  
- **`fips`**: 5-digit FIPS county code.  
- **`place_code`**: FEMA's internal location code.  
- **`designated_area`**: Name or description of the affected area (e.g., "Statewide").  
- **`declaration_request_number`**: Unique ID for the disaster declaration request.  
- **`hash`**: MD5 hash of the record.  
- **`last_refresh`**: Date the record was last updated by FEMA.  
- **`id`**: Unique ID for the record.  

#### M5-Specific Dataset (`us_disasters_m5.csv`):
- Contains a subset of columns from the full dataset, filtered for CA, TX, and WI.  
- Additional constraints: Disasters must have begun before May 23, 2016, and ended on or after January 29, 2011.  

---

### Acknowledgements
All credit for the dataset goes to the **Federal Emergency Management Agency (FEMA)** for building and maintaining this valuable resource.

---

### Usage
This dataset is ideal for:
- Exploratory Data Analysis (EDA) of natural disaster trends over time.  
- Visualizing disaster frequency, types, and geographic distribution.  
- Analyzing the impact of disasters on specific states or counties.  

---

Feel free to explore the data and contribute to this repository! If you have any questions or suggestions, please open an issue or submit a pull request.

---
