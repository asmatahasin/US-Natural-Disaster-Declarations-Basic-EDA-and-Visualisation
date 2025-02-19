# US-Natural-Disaster-Declarations-Basic-EDA-and-Visualisation
County-level data from the Federal Emergency Management Agency: 1953 - today
About Dataset
Context

The United States experience a large variety of natural disasters each year: devastating hurricanes, seasonal tornadoes, and scorching wild fires are among the events that endanger many lifes and cause billions of dollars in damages. The Federal Emergency Management Agency (FEMA) is in charge of "helping people before, during, and after disasters" by coordinating disaster response and providing relief funds.

Content:
This summary dataset is a high-level summary of all federally declared disasters since 1953. I downloaded it from the FEMA website and applied a few simple data cleaning and formatting measures. 

us_disaster_declarations.csv: the full dataset with all rows and columns. The geographical resolution is the county level, with FIPS codes being used to encode the counties. In addition to the fips and timing features, the data provides the type of disaster and also binary flags that indicate whether specific aid programs were triggered in response.

Column Description

Most of those descriptions have been taken verbatim from the FEMA website. I added small clarifications to some of them:

Full dataset us_disaster_declarations.csv:

fema_declaration_string: Agency standard method for uniquely identifying Stafford Act declarations. Concatenation of declaration_type, disaster_number and state.
disaster_number: Sequentially assigned number used to designate an event or incident declared as a disaster.
state: US state, district, or territory.
declaration_type: One of "DR" (= major disaster), "EM" (= emergency management), or "FM" (= "fire management")
declaration_date: Date the disaster was declared.
fy_declared: Fiscal year in which the disaster was declared.
incident_type: Type of incident such as "Fire", "Flood", or "Hurricane". The incident type will affect the types of assistance available.
declaration_title: Title for the disaster. This can be a useful identifier such as "Hurricane Katrina" or "Covid-19 Pandemic".
ih_program_declared: Binary flag indicating whether the "Individuals and Households program" was declared for this disaster.
ia_program_declared: Binary flag indicating whether the "Individual Assistance program" was declared for this disaster.
pa_program_declared: Binary flag indicating whether the "Public Assistance program" was declared for this disaster.
hm_program_declared: Binary flag indicating whether the "Hazard Mitigation program" was declared for this disaster.
incident_begin_date: Date the incident itself began.
incident_end_date: Date the incident itself ended. This feature has about 14% NA entries.
disaster_closeout_date: Date all financial transactions for all programs are completed. This column has 98% NA entries.
fips: 5-digit FIPS county code; used to identify counties and county equivalents in the United States, the District of Columbia, US territories, outlying areas of the US and freely associated states. Concatenated from the 2 source columns "fipsStateCode" and "fipsCountyCode".
place_code: A unique code system FEMA uses internally to recognize locations that takes the numbers '99' + the 3-digit county FIPS code. There are some declared locations that don't have recognized FIPS county codes in which case a unique identifier was assigned.
designated_area: The name or phrase describing the U.S. county that was included in the declaration. Can take the value "Statewide".
declaration_request_number: Unique ID assigned to request for a disaster declaration.
hash: MD5 Hash of the fields and values of the record.
last_refresh: Date the record was last updated by FEMA.
id: Unique ID assigned to the record. Those last 4 columns are primarily for bookkeeping.
M5-specific dataset us_disasters_m5.csv:

disaster_number: Sequentially assigned number used to designate an event or incident declared as a disaster.
state: One of the three states "CA", "TX", or "WI".
declaration_type: One of "DR" (= major disaster), "EM" (= emergency management), or "FM" (= "fire management")
declaration_date: Date the disaster was declared.
incident_type: Type of incident such as "Fire", "Flood", or "Biological". The incident type will affect the types of assistance available.
declaration_title: Title for the disaster.
ih_program_declared: Binary flag indicating whether the "Individuals and Households program" was declared for this disaster.
ia_program_declared: Binary flag indicating whether the "Individual Assistance program" was declared for this disaster.
pa_program_declared: Binary flag indicating whether the "Public Assistance program" was declared for this disaster.
hm_program_declared: Binary flag indicating whether the "Hazard Mitigation program" was declared for this disaster.
incident_begin_date: Date the incident itself began.
incident_end_date: Date the incident itself ended. The M5 constraint is that the disaster must have begun before the start of the evaluation time period on 2016-05-23 and ended on or after the begin of the training data range on 2011-01-29. This feature has about 14% NA entries, which were considered under the assumption that start data = end date.
fips: 5-digit FIPS county code; used to identify counties and county equivalents in the United States, the District of Columbia, US territories, outlying areas of the US and freely associated states. Concatenated from the 2 source columns "fipsStateCode" and "fipsCountyCode".
designated_area: The name or phrase describing the U.S. county that was included in the declaration.

Acknowledgements:
All the credit goes to FEMA for building and maintaining this dataset.
