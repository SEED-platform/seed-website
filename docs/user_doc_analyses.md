There are several analyses that can be run on properties.  Expand the sections below to learn more about each analysis.

??? note "EUI Analysis"
	## EUI Analysis

	details coming soon.

??? note "CO2 Analysis"
	## CO2 Analysis

	details coming soon.

??? note "BETTER Analysis"
	## BETTER Analysis

	details coming soon.

??? note "Energy Equity & Environmental Justice (EEEJ) Analysis"
	## Energy Equity & Environmental Justice (EEEJ) Analysis

	details coming soon.

??? note "BSyncr" Analysis"
	## Bsyncr Analysis

	details coming soon.

??? note "Element Statistics Analysis"
	## Element Statistics Analysis

	details coming soon.

??? note "Building Upgrade Recommendation Analysis"
	## Building Upgrade Recommendation Analysis

	The Building Upgrade Recommendation Analysis is a workflow that can be used to identify what types of upgrades could be performed on selected buildings based on specific parameters such as year built, gross floor area, EUI, etc. Buildings can then be prioritized based on the results of the analysis.

	The workflow implemented is depicted in the following diagram:

	![Building Upgrade Recommendation decision tree](images/building_upgrade_rec.png){:.seed-img}

	The configurable parameters are defined as:

	- **A** the Total EUI Goal for the building (including Electricity, Gas, Etc.)
	- **B** the Year Built Threshold - The year built to use as a comparison threshold
	- **C** the Poor Actual to Benchmark EUI Ratio - The poor ratio of Total EUI to Benchmark Total EUI value to use. Ratio = Total EUI/Benchmark EUI
	- **D** the Building Square Footage Threshold - The gross square footage to use as a comparison threshold
	- **E** the Fair Actual to Benchmark EUI Ratio - The fair ratio of Total EUI to Benchmark Total EUI value to use. Ratio = Total EUI/Benchmark EUI
	- **F** the Fossil Fuel EUI Goal - The Fossil Fuel EUI Goal for the building
	- **G** the Fossil Fuel-Fired Equipment RSL Threshold - The remaining service life value to use for your fossil fuel-fired equipment as a comparison threshold in the calculations.
	- **H** the Condition Index Threshold - The condition index to use as a comparison threshold

	### Analysis Pre-requisites

	The analysis requires certain data to be available in SEED:

	- Year Built 
	- Gross Floor Area
	- Total building EUI
	- Building Gas EUI
	- Building Electricity EUI
	- Building actual energy use
	- ASHRAE Electricity EUI Target
	- ASHRAE Gas EUI Target
	- Condition Index of the building
	- If a building has Building Automation System (BAS) - represented by counting the elements of time 'D.D.C Control Panel'
	- The fossil fuel-fired element with the lowest remaining service life

	### Running the analysis

	1. From the inventory page, select the buildings in the table that you want to run the analysis on

	2. From the Actions dropdown menu, select "Run an Analysis"

	3. In the Run an Analysis modal, enter the name of the analysis and select "Building Upgrade Recommendation as the type"

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