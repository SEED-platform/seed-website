There are several analyses that can be run on properties.  Expand the sections below to learn more about each analysis.

??? note "Overview"
	## Analysis Overview

	There are currently six different types of Analyses available in SEED:

	- **BSyncr**
		- Makes a Building Sync file from the property data in SEED to be used with the NMEC (Normalized Metered Energy Consumption) program
		- Algorithms are based on methods in this Github repository
		[NMECR Github Repo](https://github.com/kW-Labs/nmecr) 
	- **BETTER**
		- Runs a BETTER analysis from the property data in SEED
		[BETTER web Tool](https://better.lbl.gov/)
	- **EUI**
		- Calculates the EUI of a property based on the meter data and the gross floor area
	- **Average Annual CO2**
		- Calculates the CO2 emissions of a property based on the meter data and the eGRID region (which is based on the location of the property)
	- **Energy Equity & Environmental Justice (EEEJ)**
		- The Energy Equity & Environmental Justice analysis retrieves EEEJ information and indicators for your properties from various sources
	- **Element Statistics**

	## Generating an Analysis
	- In the Property List, select the properties you want to perform an analysis on
	- Select Run Analysis from the Actions menu choice

	![](images/analyses_general_01.png)

	- Add an Analysis Name and select the Analysis Type

	![](images/analyses_general_02.png)

	- Depending on the analysis type, there will be various other parameters to set
	(see the sections below for each Analysis Type details)

	- Start the Analysis
	- Using the left Navigation bar, go to the Analyses section of SEED to see the results

	![](images/navButton_analyses.png)

	![](images/analyses_general_03.png)

??? note "BSyncr" Analysis"
	## Bsyncr Analysis

	the BSyncr analysis option makes a Building Sync file from the property data in SEED to be used with the NMEC (Normalized Metered Energy Consumption) program. Algorithms are based on methods in this Github repository
	[NMECR Github Repo](https://github.com/kW-Labs/nmecr) 

	### Setting up the Analysis

	- In the Property List, select the properties you want to perform an analysis on
	- Select Run Analysis from the Actions menu choice
	- Add an Analysis Name and set Type = BSyncr

	![](images/analyses_BSyncr_setting_up_analysis.png)

	### Running the Analysis

	- Click the “Create Analysis” button to start the analysis
	- Go to the Analyses page (from the left Navigation bar) to see the status of the analysis

	![](images/navButton_analyses.png)

	![](images/analyses_BSyncr_running_analysis.png)

	### Viewing the Analysis Results

	On the Analyses page, it is possible to click on the BSyncr analysis name, and see the individual analyses, and then click on the Run IDs for each property to see the details for that property.

	![](images/analyses_BSyncr_viewing_analysis_results.png)
	![](images/analyses_BSyncr_viewing_analysis_results_02.png)

	
??? note "BETTER Analysis"
	## BETTER Analysis

	The Building Efficiency Targeting Tool for Energy Retrofits (BETTER) is a software toolkit that enables building operators to quickly and easily identify the most cost-saving eneryg efficiency measures in buildings and portfolios using readily available guilding and eneryg data. For more details, see the [BETTER website](https://better.lbl.gov/).

	BETTER can be used to quickly assess the potential energy savings in a building, which then allows users to filter for the buildings with the hightest potential savings, and target those buildings for a more detailed energy audit.

	It is possible to run BETTER from the SEED Property Inventory List view, and then view the results.

	### Analysis Pre-requisites

	In order to run a BETTER analysis from SEED on a building, the following data must be imported into the Property Inventory

	#### Data mapping on import 
	Several fields must be properly mapped when imported into SEED in order to have the correct information for a BETTER analysis. 
	
	**Property Type**
	The Property Type must be mapped (for example from the ENERGY STAR Portfolio Manager field called "Property Type - Self Selected") and must be set to a "Space Type" recognized by BETTER. 
	See the [BETTER FAQ web page, Building Spaces Types section](https://better.lbl.gov/docs/faq/){:.external}section for the latest space types, as new types are added frequently. 

	**Address Data**
	The Address data for the property must be mapped properly on import, according to the following fields, in order to correctly set the location and weather data that BETTER will use for the analysis.

	- 'Address Line 1' field
	- 'City' and 'State' fields OR 'Postal Code' field
	
	![](images/analyses_BETTER_DataFieldMapping.png)

	#### Monthly meter data

	- 12 months (or more) of consecutive meter data, for either gas or electricity, or both. This data is available from ENERGY STAR Portfolio Manager, which is one of the easiest methods for importing the data into SEED.

	#### BETTER account settings
	
	When a BETTER account is created, an API token can be generated in the "My Profile" section of the BETTER account. This is used in SEED to connect to BETTER in the background to run a BETTER analysis on a property in SEED.

	![](images/analyses_BETTER_API_01.png)

	In SEED, this API token is then entered into the Organizations/Settings in the "BETTER Analysis API Key" section

	![](images/analyses_BETTER_API_02.png) 

	### Running the Analysis

	1. In the Inventory List, select one or more properties on which you want to perform a BETTER analysis, and select ‘Run Analysis’ from the Actions dropdown menu
	![](images/analyses_BETTER_select_analysis.png)

	3. The **Run Analysis** dialog box will appear. Add a descriptive name for the current analysis, and set **Type** to **BETTER**
	![](images/analyses_BETTER_select_analysis_settings_01.png)

	4. Setting **Type** to **BETTER** causes more settings to be displayed. 
	
	![](images/analyses_BETTER_select_analysis_settings_02.png)

	5. When all the settings have been properly defined, click the **Create Analysis** button to start the analysis running. Clicking on the Analyses navigation button will go to the Analyses page, where the currently running analysis is shown. The **Run Status** column shows the progress of the analyses

	![](images/analyses_BETTER_select_analysis_running.png)

	6. Viewing the BETTER results
	On the Analyses page, click on the Analysis Name which will then display the results for each individual property.

	![](images/analyses_BETTER_select_analysis_results_01.png)

	![](images/analyses_BETTER_select_analysis_results_02.png)

	SEED will display the reports in the same way as they would be displayed in BETTER.
	Click the **Run ID** link to see the reports

	![](images/analyses_BETTER_select_analysis_results_03.png)

	Clicking on the Property link will display the Property Detail page for that property with the BETTER Analysis details added

	![](images/analyses_BETTER_select_analysis_results_04.png)

	One the Property Detail page, clicking on the Analyses link will show all the analyses for this property

	![](images/analyses_BETTER_select_analysis_results_05.png)

	SEED also saves many of the BETTER results in fields, which can then be added to the results display in both the Property List and Property Detail views

	![](images/analyses_BETTER_select_analysis_results_06.png)

??? note "EUI Analysis"
	## EUI Analysis

	### Setting up the Analysis

	- In the Property List, select the properties you want to perform an analysis on
	- Select Run Analysis from the Actions menu choice
	- Add an Analysis Name and set Type = EUI

	![](images/analyses_EUI_setting_up_analysis.png)

	### Running the Analysis

	- Click the “Create Analysis” button to start the analysis
	- Go to the Analyses page to see the status of the analysis

	![](images/analyses_EUI_running_analysis.png)

	### Viewing the Analysis Results
	On the Analyses page, it is possible to click on the EUI analysis name, and see the individual analyses

	![](images/analyses_EUI_viewing_analysis.png)

	Then click on the Run IDs for each property to see the details for that property.

	![](images/analyses_EUI_viewing_analysis_02.png)

	In the Property List view, the field Analysis EUI is added to show the calculated value. 
	
	If the value is blank, it means that there was not meter data to calculate the value

	![](images/analyses_EUI_viewing_analysis_03.png)

??? note "Average Annual CO2 Analysis"
	## Average Annual CO2 Analysis

	### Data Import

	- In the Property data being imported to SEED, for a CO2 analysis the following must be added
		- eGRID Subregion Code
			- Find the eGRID Subregion definitions here
			[eGRID Subregion Codes](https://www.epa.gov/egrid/summary-data)

	![](images/analyses_co2_setting_up_analysis-egrid.png)

	### Setting up the Analysis

	- In the Property List, select the properties you want to perform an analysis on
	- Select Run Analysis from the Actions menu choice
	- Add an Analysis Name and set Type = Average Annual CO2

	![](images/analyses_co2_setting_up_analysis.png)

	### Running the Analysis

	- Click the “Create Analysis” button to start the analysis
	- Go to the Analyses page (from the left Navigation bar) to see the status of the analysis

	![](images/analyses_co2_running_analysis.png)

	### Viewing the Analysis Results
	On the Analyses page, it is possible to click on the CO2 analysis name, and see the individual analyses

	![](images/analyses_co2_viewing_analysis.png)

	Then click on the Run ID or the Property link for each property to see the details for that property.

	![](images/analyses_co2_viewing_analysis_02.png)

	In the Property List view, the fields “Average Annual CO2” and “Average Annual CO2 Coverage” contain the CO2 results in the Inventory Property List View.
	
	![](images/analyses_co2_viewing_analysis_03.png)

??? note "Energy Equity & Environmental Justice (EEEJ) Analysis"
	## Energy Equity & Environmental Justice (EEEJ) Analysis

	The Energy Equity & Environmental Justice analysis retrieves EEEJ information and indicators for your properties from various sources including:

	- [The Climate and Economic Justice Screening Tool](https://screeningtool.geoplatform.gov/en/methodology){:.external}
	- [Environmental Justice Screening and Mapping Tool (EJScreen)](https://www.epa.gov/ejscreen){:.external}
	- [The U.S. Department of Housing and Urban Development](https://hudgis-hud.opendata.arcgis.com/){:.external}

	### Analysis Pre-requisites

	The analysis requires certain data to be available in SEED in order to run successfully. The name of these fields is important at this time.

	- 'Address Line 1' field
	- 'City' and 'State' fields OR 'Postal Code' field
	- Optional: 'Latitude' and 'Longitude' from geocoded property

	The analysis workflow uses the [Census geocoder API](https://geocoding.geo.census.gov/){:.external} to retrieve each property's census tract based on the Address Line 1 + either City/State or Postal Code information. If the property has already been geocoded, this information will instead be used to determine the census tract.

	Note that the census geocoder API is a bit slow. Selecting less than 20 properties at a time for teh analysis or geocoding the properties with the MapQuest API prior to running the analysis is recommended.

	Once the census tract is determined

	### Running the Analysis

	1. First select one or more properties on the inventory list page and then choose ‘Run Analysis’ from the Actions dropdown menu:

		![Select Run an Analysis from the Actions Menu](images/eeej_1.webp){:.seed-img}

	2. In the modal window that will appear, name your analysis and select “Energy Equity & Environmental Justice (EEEJ)” as the Type of analysis from the dropdown menu:

		![Name your analysis and select EEEJ as the type](images/eeej_2.webp){:.seed-img}

	3. Messages indicating an error or a successful analysis creation will be displayed in the top right corner of the page. You can click the link in the message at the top right of the screen “Click here to view your analyses”. Or you can navigate to the Analyses page from the left navigation menu.

		![Navigate to your analysis](images/eeej_3.webp){:.seed-img}

	4. On the Analyses page you can see a list of analyses run and their status: 

		![List of analyses](images/eeej_4.webp){:.seed-img}

	5. Click on the analysis name to access more details about the analysis. You can read a small description of the analysis explaining where the data came from at the top of the page. To see details about a specific property, click on the run ID next to the property:

		![Click on run ID for details page](images/eeej_5.webp){:.seed-img}

		Details for a property include:

		- Latitude, Longitude, and Census Tract retrieved from the Census Geocoder service
		- Whether a property is classified as disadvantaged (DAC) according to the CEJST data
		- Whether a property is low income according to CEJST data
		- Whether a property is classified as having an energy burden and being low income according to CEJST data
		- The percentile of energy burden according to CEJST data
		- The share of neighboring disadvantaged tracts according to CEJST data
		- The number of affordable housing locations in the identified census tract according to HUD datasets on multi-family assisted housing and public development housing.
		- A link to the EJ screen report generated for a 1-mile area around the property

		![Analysis details page](images/eeej_6.webp){:.seed-img}

		An example EJ Screen report:

		![Example EJ Screen report](images/eeej_7.webp){:.seed-img}

	6. As part of the analysis, the result fields above (except for the EJ Screen Report Link) have been saved directly to each property:

		![Analysis results saved to property fields](images/eeej_8.webp){:.seed-img}

	7. Additionally, an Analysis "Card" is saved at the top of the individual Property Detail page (note that this shows only the last analysis run, but all analyses can be accessed from the Analyses menu).

		![Analysis card at the top of the property detail page](images/eeej_9.webp){:.seed-img}

	8. The disadvantaged census tracts can be visualized on the map page (the areas with blue shading):

		![SEED map showing disadvantaged community census tracts](images/eeej_10.webp){:.seed-img}


??? note "Element Statistics Analysis"
	## Element Statistics Analysis

	details coming soon.

??? note "Building Upgrade Recommendation Analysis"
	## Building Upgrade Recommendation Analysis

	The Building Upgrade Recommendation Analysis is a workflow that can be used to identify what types of upgrades could be performed on selected buildings based on specific parameters such as year built, gross floor area, EUI, etc. Buildings can then be prioritized based on the results of the analysis.

	The workflow implemented is depicted in the following diagram:

	![Building Upgrade Recommendation decision tree](images/upgrade_rec_flowchart.webp){:.seed-img-lg}

	The configurable parameters are defined as:

	- **Total EUI Goal** - The Total EUI Goal for the building (including Electricity, Gas, Etc.)
	- **Year Built Threshold** - The year built to use as a comparison threshold
	- **Poor Actual to Benchmark EUI Ratio** - The poor ratio of Total EUI to Benchmark Total EUI value to use. Ratio = Total EUI/Benchmark EUI
	- **Fair Actual to Benchmark EUI Ratio** - The fair ratio of Total EUI to Benchmark Total EUI value to use. Ratio = Total EUI/Benchmark EUI
	- **Building Square Footage Threshold** - The gross square footage to use as a comparison threshold
	- **Fossil Fuel EUI Goal** - The Fossil Fuel EUI Goal for the building
	- **Fossil Fuel-Fired Equipment RSL Threshold** - The remaining service life (RSL) value to use for your fossil fuel-fired equipment as a comparison threshold in the calculations.
	- **Condition Index Threshold** - The condition index to use as a comparison threshold

	### Analysis Pre-requisites

	The analysis requires certain data to be available in SEED in order to run successfully:

	- Year Built 
	- Gross Floor Area
	- Total Building EUI
	- Building Gas EUI
	- Building Electricity EUI
	- Building actual energy use
	- ASHRAE Electricity EUI Target
	- ASHRAE Gas EUI Target
	- Condition Index of the Building
	- Whether a building has a Building Automation System (BAS) - represented by counting the elements of type 'D.D.C Control Panel'
	- The fossil fuel-fired element with the lowest remaining service life

	The analysis will allow a user to select which fields to use for the information above, with the exception of "Year Built" and "Gross Floor Area": the canonical SEED fields "Year Built" and "Gross Floor Area" are automatically used to capture this information.

	### Running the Analysis

	1. From the inventory page, select the properties in the table that you want to run the analysis on

	2. From the Actions dropdown menu, select "Run an Analysis"

	3. In the Run an Analysis modal, enter the name of the analysis and select "Building Upgrade Recommendation" as the type

	4. Once the type is selected, the modal will expand with options to set the configurable thresholds for the workflow. Fill out these values and click 'Create Analysis'
	 ![Analysis Configuration Modal](images/upgrade_rec_analysis.webp){:.seed-img-sm}

	5. The analysis will be created and a link will appear in the top right corner to take you directly to the analysis page. You can also access the Analyses from the "Analysis" left navigation menu.
	 ![Analysis Configuration Modal](images/view_analysis.webp){:.seed-img-sm}

	6. On the analysis page you can see details about the analysis, a list of properties that were run, and links to see individual results.

	7. On the individual property analysis results page, you can see similar information related to the configuration details and results.
		 ![Analysis Detail Page](images/analysis_details.webp){:.seed-img}  

	8. This analysis adds the field 'Building Upgrade Recommendation' to the analysis. 
		 ![Analysis Fields on Inventory List Page](images/analysis_fields.webp){:.seed-img}

		The values entered in this field can be used to prioritize your buildings list. (For example, by filtering the inventory list by 'Deep Energy Retrofit' and labeling the resulting list of buildings with a particular label.) As shown in the diagram above, the possible values for this field are:

		- Deep Energy Retrofit
		- Equipment Replacement
		- Re-tuning
		- No DER Project Recommended
		- Missing Data