# Release Notes

In addition to the [GitHub release notes](https://github.com/SEED-platform/seed/releases) page, this page provides more details on the changes made in each version of SEED-Platform by version number.

If you have any questions about releases or changes to the program, please contact us using one of the methods on the [contacts page](contact.md).

??? note "**Version 2.20.1**"

	## Version 2.20.1

	The full release history can be found on the SEED Github Repository

	- [https://github.com/SEED-platform/seed/releases/tag/v2.20.0](https://github.com/SEED-platform/seed/releases/tag/v2.20.0)

	- [https://github.com/SEED-platform/seed/releases/tag/v2.20.1 (patch release)](https://github.com/SEED-platform/seed/releases/tag/v2.20.1)

	## Updates

	### Inventory

	**Property Detail** 
		
	- **Audit Template:** It is now possible to upload and download a BuildingSync or Audit Template file

		![](images/inventory_property_auditTemplate.png)
	
	### Data 

	- A change was made to that now **it is not possible to delete matching field criteria after importing data, so the matching fields must be set in Column Settings before importing data**
		- New matching fields can be ADDED, but existing matching fields can not be DELETED.
	- **Address line 1** is no longer a default matching field

	###Analyses

	**Property Detail:** Analyses can now be run from the Property Detail page, using the Analyses link

	![](images/analyses_propDetail.png)

	**Property List:** Analyses are now associated with the cycles they were simulated in, so the results can be viewed by cycle

	**BETTER:** it is now possible to specify what meter data to be used in the analyses
	
	- **A specific cycle**

		![](images/BETTER_cycle.png)

	- **A range of dates**

		![](images/BETTER_cycle_dateRange.png)

	- **All the meter data**

		![](images/BETTER_cycle_allMeterData.png)

	## New Features

	### Analyses

	#### EEEJ -- Energy Equity and Environmental Justice

	SEED now has an Analyses feature that will show buildings that are in disadvantaged communities using data from: 

	- US Census Bureau census tract data
	- [Climate and economic Justice Screening Tool](https://screeningtool.geoplatform.gov/en#3/33.47/-97.5)

		![](images/EEEJ_climateJusticeScreeningTool.png)

	To run an EEEJ analysis, do the following:

	- **Property List view**

		- **Select the properties for the analysis**
		- **Actions pulldown list**
			- Give the analysis a name and select the “Energy Equity & Environmental Justice (EEEJ) option

		![](images/EEEJ_runAnalyses.png)

	To view the results:
		
	- **Analyses**

		- The results will be be displayed in the Analyses screen

		![](images/EEEJ_analyses_results.png)

		- Click on the Run ID in the analysis list to see individual building results

		![](images/EEEJ_analyses_results_bldg.png)

	- **Inventory**

		- **Property List and Detail View:** Results are displayed in the Inventory Property List and Detail view in these fields

			![](images/EEEJ_inventory_prop_results.png)

		- **Property List View:** Results are also displayed on the Inventory List Map

		![](images/EEEJ_inventory_prop_map.png)

		- **Property Detail:** 

			- Results are displayed in the Property Detail view in "card" format
			- It is also possible to run Analysis for a specific property from the Property Detail view

			![](images/EEEJ_inventory_prop_detail.png)

	### Data

	#### Batch Import of Audit Template Files

	It is now possible to import properties directly from an Audit Template record

	- **Organization / Settings:**

		- Input the information about the Audit Template account under the Audit Template option in Organizations/Settings
		- The Audit Template Documentation, linked from that Organizations/Settings screen, will explain how to get the Organization Token.

		![](images/AT_import_org_settings.png)

	- **Data**

		- When adding data, there is an option to "Import Audit Template Buildings"
		- Based on the values input in Organization/Settings for Audit Template, the appropriate buildings will be displayed and can be selected for import

		![](images/AT_import_data.png)


??? note "**Version 2.19.0**"

	## Version 2.19.0

	## Updates

	### Insights

	**Default Reports** 
		
	- The reports that used to be accessed from the Inventory List view are now in Insights
		
		![](images/insights_default_reports-1000.png)

	- The export from those reports now includes the matching fields

		![](images/insights_default_reports_export.png)

	**Program Overview** 
		
	- Clicking on the Program Overview column goes to the Property Insights graphs
	- Percentages are displayed for Compliant and Non-Compliant sections of the graphs

		![](images/insights_overview2insights.png)

	**Property Insights** 
		
	- A column for the X and Y axis have been added in the table below the graph that lists all the properties

		![](images/insights_propertyInsights_XY.png)


	### Salesforce

	**Scheduled Daily Update:** The "Sync Salesforce" button that used to be in the Organizations/Salesforce setup has been removed because of timeout issues.

	![](images/org_settings_Salesforce_syncbutton.png)

	## New Features

	### About / Terms of Service

	The About screen now has a link to a "Terms of Service"

	![](images/about_termsOfService.png)

	### Data Import

	**Multiple Cycle Upload:** 

	The Data Import dialog box now has an option for importing data across multiple cycles
	
	- **Year Ending:** SEED uses the **Year Ending** field to determine the cycle that the record belongs to
		- If any record does not have a **Year Ending** field, SEED will automatically assign it to the "Default Cycle" specified int he data import dialog box
	- **Cycles:** Cycles for the **Year Ending** definitions need to be pre-defined

	![](images/data_import_multiCycle.png)

	Once the data is imported, **Cross Cycles** (Inventory List view) will show how the records were assigned to different cycles

	![](images/inventory_property_crossCycle.png)

	The Inventory List view Cross Cycle results show for each property, which cycle the property was imported into.

	- **Property ID 2045373:** Based on the Year Ending field, there is one record for this building in all four cycles
	- **Property ID 2045374:** This record did not have data in the Year Ending field so it was imported into the Default Cycle of 2021 Calendar Year

		![](images/inventory_property_crossCycle_results.png)

	### Inventory

	**UBID Support:** 

	It is now possible to have multiple UBID values defined for a property, and to select the one that most accurately represents the building footprint

	![](images/inventory_property_detail_UBID-1.png)

	The UBID marked "Preferred" will be displayed with the SEED Map as an underlay. 

	![](images/inventory_property_detail_UBID-2.png)

	The UBID centroid and bounding box for the "Preferred" UBID will also be displayed in the Inventory List Map view

	![](images/inventory_property_detail_UBID-3.png)

	**Geocoding Fields Added:** 

	If a property is geocoded, the new Geocoding fields are now added to the Property

	![](images/inventory_property_geocoding_fields.png)


??? note "**Version 2.18.0**"

	## Version 2.18.0

	## Updates

	### Inventory

	**Analyses / EUI:** It is now possible to select all the meter data, a date range, or a cycle for this analysis

	![](images/EUI_meterdata_options.png)

	### Insights

	**Program Setup:** Select Cycles instead of start and end dates

	![](images/insights_program_setup_cycles.png)

	## Known Issues

	### Inventory

	**List View:** In the Property tab, it is not possible to sort on Tax Lot fields, and vice versa

	![](images/inventory_property_noTaxLotSort.png)

	## New Features

	### Inventory

	**List View** 
	
	- **Salesforce:** It is now possible to run Salesforce from the Actions menu on selected properties

		![](images/inventory_property_list_Salesforce.png)

	- **Export GeoJSON:** Meter data has been added to the GeoJSON file that is exported from SEED

		![](images/inventory_property_export_geoJSON_meters.png)

	**Detail View** 
	
	- **Salesforce:** It is now possible to run Salesforce on individual properties from the Inventory Property Detail view

		![](images/inventory_property_detail_Salesforce.png)

	- **Timeline:** This feature allows viewing actions, such as importing Audit Template records, over time

		![](images/inventory_property_detail_timeline-1.png)

		There is a row in the Timeline for ever event
		Events added to the Timeline are

		- New Notes (added manually)
		- New Analyses
		- New Audit Template or BuildingSync file upload
		
		Clicking the Timeline link for a property will show all the actions across cycles
		
		![](images/inventory_property_detail_timeline-1.png)

		Click the Expand All button to see the details of each event

		![](images/inventory_property_detail_timeline-2.png)
		![](images/inventory_property_detail_timeline-3.png)
		![](images/inventory_property_detail_timeline-4.png)
		![](images/inventory_property_detail_timeline-5.png)

		**Audit Template Import:** Audit Template and BuildingSync files can be imported in the Inventory Property Detail view

		![](images/inventory_property_detail_auditTemplateImport.png)

		**Audit Template Delete Scenarios:** Audit Template Scenarios can be deleted in the Inventory Property Detail view

		![](images/inventory_property_detail_auditTemplate_delete_scenario.png)

	### Insights

	**Property Insights** 
	
	Labels can now be added to properties displayed in Property Insights

	![](images/insights_propertyInsights_add_labels.png)

	### Organizations / Settings

	**Salesforce** 
	
	Salesforce can now be configured within SEED in Organizations / Settings / Salesforce

	![](images/org_settings_Salesforce-1.png)
	![](images/org_settings_Salesforce-2.png)
	![](images/org_settings_Salesforce-3.png)
	![](images/org_settings_Salesforce-4.png)
	![](images/org_settings_Salesforce-5.png)


??? note "**Version 2.17.2**"

	- [Release Notes v2.17.2](resources/SEED Platform V2_17_2 Release Notes.pdf)

	## Version 2.17.2

	## Updates

	### Inventory

??? note "**Version 2.5.0**"

	## Version 2.5.0

	### Data Import

	#### New Features

	- **Upload a GeoJSON File:** This option allows importing a file with GIS location data in the GeoJSON format

		![Upload GeoJSON image v2.5.0](images/release_notes/UploadGeoJSON.png)

	- **Performance improvements:** In general, importing files should be much faster, even for cases with many thousand records.

	- **Upload BuildingSync Data:** Updated the import to BuildingSync Version 1.0

	### Mapping and Matching

	#### New Features

	- **ULID added as a matching field:** Unique Land ID (ULID) has been added as a matching field for Tax Lot data. This is comparable to the Unique Building ID (UBID) matching field for Property data

		![matching fields image v2.5.0](images/release_notes/UBID-ULID-Matching.png)

??? note "**Version 2.4.0**"

	## Version 2.4.0

	### Data Import

	#### Changes

	- **Import Portfolio Manager Data:** This option allows users to log into their ENERGY STAR&reg; Portfolio Manager&reg; account and specify the Custom Report Template from which to download data

	- **Upload BuildingSync Data:** A BuildingSync file is an XML file with building information in it, which is generated by several programs, including DOE's Asset Score. SEED can now import some variations of that XML file.

		![Data Upload image v2.4.0](images/release_notes/Data-Upload.png)

	- **File importing improvements:** General improvements for handling files with carriage returns, blank lines, unusual characters

	- **Performance improvements:** In general, importing files should be much faster, even for cases with many thousand records.

	#### Known Issues

	- **Upload BuildingSync Data:** The program doesn't currently support all possible variations on a BuildingSync file.

	### Mapping and Matching

	#### New Features

	- **Column Settings (under Organizations):**  It is now possible to change the field mapping of existing data in the organization, as well "Merge Protection" which prevents specific fields (that may have been edited by hand) to be overwritten by newly imported data. For more details, see Organizations below.

	- **Column Mappings (under Organizations):** It is now possible to change the default mappings for data to be imported. For more details, see Organizations below.

	#### Changes

	- **Performance Improvements:** Matching should generally be faster than in previous versions

	### Inventory List View

	#### Changes

	- **Performance Improvements:** Loading the inventory list has been very time-consuming, particularly with large datasets or large numbers of columns. This has been improved drastically.

	### List Settings

	#### Bug Fix

	- **Field order maintained on save:** In previous versions, when saving the List Settings after a change, the program would reverse the field order while still in List Settings view (although not in the actual view the settings controlled). This has been fixed in this version.

	### Organizations

	#### New Features

	There are two new options in the Organization section of the program: Column Settings and Column Mappings

	![New Organization Options v2.4.0](images/release_notes/NewOrgOptions.png)

	- **Column Settings:** This is a new screen which allows users 1) change the display name of a column that already exists in the database, and 2) specify what fields should be protected from having new data replace existing data.

		![Column Settings v2.4.0](images/release_notes/ColumnSettings.png)

	- **Column Mappings:** This screen shows the stored default mappings for files that have been previously imported, which is the default mapping for these fields when new files are imported in the future.  If problems are found in the mappings here, the bad mappings should be deleted so that when new files with these fields are imported, those same mapping mistakes will not be made again. Changing the mappings here does not affect existing data, it only affects the default mapping settings for data that will be imported in the future.

		![Column Mappings v2.4.0](images/release_notes/ColumnMappings.png)

??? note "**Version 2.0.0**"

	## Version 2.0.0

	### Data Model

	#### Changes

	- The data is now stored in two table structures, one for Tax Lot/Parcel information, one for Property/Building Information

	- Each record in those tables is associated with a time period called a Cycle, which can correspond to a benchmarking compliance cycle.

	### Navigation Bar

	#### Changes

	- **Projects:** disabled for the current release because we want to work with users to make sure we have a feature that solves user needs, which the previous iteration of Projects may not have. 

	- **Inventory:** BUILDINGS is now INVENTORY, because the program is now storing and displaying data from the perspective of Tax Lot/Parcel and Property/Building.

	- **API Documentation:** added an implementation of the Swagger API framework to display the program API structure for developers.

	- **Log Out:** moved Log Out to the last option of the Navigation bar from an option in the user account, which makes it more straightforward to log out of the program

		![Menu image v2.0.0](images/release_notes/menu.png)

	### Data Import

	#### Changes

	- **Specify Time Period/Cycle:** Each time a file is imported, it must be associated with a Time Period/Cycle. 

		![data import images v2.0.0](images/release_notes/data_import.png)

	#### Known Issues

	- **Green Button Data:** Green Button Data upload is disabled. This feature is being reworked.

	### Mapping

	#### Changes

	- **Assign fields to Property / Tax Lot:** The new data model requires that during field mapping, each field be assigned to either the Property or the Tax Lot table.	

		![mapping image v2.0.0](images/release_notes/mapping.png)

	- **Matching field names:** The Matching field name **Tax Lot ID** is now called **Jurisdiction Tax Lot ID**. The other Matching field names remain the same (**Custom ID 1**, **PM Property ID** and **Address Line 1**)

	#### Known Issues

	- **Display of mapping list is very slow when there are many fields ([1215](https://github.com/SEED-platform/seed/issues/1215)):** In some cases, such as a Portfolio Manager file with 250 fields, the program can take over a minute to display values from the pulldown list in the Mapping field, or to let you type in a field.


	### Mapping Review Screen

	#### Changes

	- **Tabs for each table:** There are now tabs for the Property and Tax Lot fields and records, depending on how the data is mapped. 

	- **All the data is loaded:** it is possible to scroll through all the records in the import file being reviewed

		![mapping review images v2.0.0](images/release_notes/mapping_review.png)

	#### Known Issues

	- **Mapped field names sometimes not shown properly:** In some cases, the actual “field name” may be displayed in the column header, such as in the case below property_type, rather than the “display name” which in this case should be Property Type. However, if there is data in the field, then the program has been able to put the data into the table.
		
		![improper mapped field names images v2.0.0](images/release_notes/known_issues_2_0.png)

	- **Property Tab when only Tax Lot data is mapped:** If Jurisdiction Tax Lot ID is mapped, there will be a View by Property tab showing just that field, when no fields were mapped to the Property table.  This is currently there by design but can be confusing. 

		![property tab v2.0.0 image](images/release_notes/property_tab_2_0.png)

	### Matching

	#### Changes

	- **Changes for New Data Model:** Matching has changed due to the new data model. Based on how field are mapped to “matching” fields, the program first does a “merge” on records and data in the same table, and then “pairs” records between the Property and Tax Lot tables.

	#### Known Issues

	- **Program Hangs on 100% Complete ([1217](https://github.com/SEED-platform/seed/issues/1217)):** When the matching has finished, the 100% Complete dialog box remains, so it is necessary to click the Cancel button to remove it and then click on the Inventory Navigation bar to see the imported/matched records

		![program hangs image v2.0.0](images/release_notes/2_0_image1.png)

	- **Matching status dialog box does not reflect correct state of data ([1221](https://github.com/SEED-platform/seed/issues/1221)):** under some circumstances, when the program finishes matching, it presents a dialog box about the status of the matching. In this version, the information on that dialog is likely to be incorrect. 

		![matching status dialog image v2.0.0](images/release_notes/2_0_image2.png)

	- **Program creates Property record even when only Tax Lot fields are mapped ([1219](https://github.com/SEED-platform/seed/issues/1219)):** under some circumstances when only matching a file to the Tax Lot table (for example if the Property tab was displayed in the Matching Review screen), the program will make an extraneous Property record that can be seen in the View by Property tab after the data has been matched.

		Sometimes this Property record is paired to a Tax Lot record, in which case if it is deleted, the Tax Lot record is also deleted

		If it is not paired to a Tax Lot record (ie, there is no “+” to the left of the record, or no value displaying in the Associated Building Tax Lot ID or Jurisdiction Tax Lot ID fields, the record can be safely deleted. 

		![matching status dialog image 2 v2.0.0](images/release_notes/2_0_image3.png)

		Click on the Checkmark column to the left of the record to select the record and then Delete Selected from the Actions pulldown list.

		![matching status dialog image 3 v2.0.0](images/release_notes/2_0_image4.png)

		When you delete the record, the program will indicate whether it is going to delete **1 property record**, or **1 property record AND 1 tax lot record** (in which case you should not proceed with the delete) 

		![matching status dialog image 4 v2.0.0](images/release_notes/2_0_image5.png)

	- **Hand Matching is not enabled:** The ability to match and unmatch records “by hand”, i.e., override the automated matching done by the program (which existed in version 1.5), is not enabled in this version of the program.

	### Inventory List View

	#### Changes

	- Rework of Buildings (now Inventory) screen: Due to the new data model, there have been significant changes to the main screen where imported data is viewed.
	See the V 2.0 Users Guide for a complete description of the new Inventory List and Detail views.

		- **Tabs:** There are two tabs, View by Property and View by Tax Lot
		- **Cycle:** Each data view is associated with a Cycle
		- **Page Title:** Title of page is now either Properties or Tax Lots, depending on which tab is selected, and no longer contains the number of records
		- **Number of records:**  the number of records is moved from the page title to the right hand side of the tab, because each tab can have different records
		- **Links at the top of the page:**
			- Buildings link (in V 1.5) is now called either Tax Lots List or Properties List, depending on which tab (Property or Tax Lot) is selected
			- **Labels:** admin link moved to Organizations
		- **All records displayed at once:** the program no longer loads just 10 - 100 records at a time. When a tab is selected, the program loads the grid with all the appropriate records
		- **Actions pulldown:** the name for the pulldown list that was called **Building Actions** is now **Actions**
		- **Filter by label:** Clicking inside this field only shows the labels that are assigned to records currently being viewed (rather than showing a list of all possible labels), based on the Cycle and Tab selected
		- **Filter Input box:** The value(s) entered into the filter boxes are applied immediately upon typing them; there no longer a need to press the **Enter** key to activate them, or click on an **Update Filters** button (in V 1.5)
		- **Sorting:** Sorting can be accomplished two different ways: 1) click the column header and it will do a simple ascending, descending or original sort; 2) click the arrow on the upper right of the column and it is possible to do hierarchical sorting (see the User Guidelines for more details)
		- **Show all, Matched and Unmatched pulldown:** This pulldown (in V 1.5) has been removed. The “+” column indicates whether there are records matched between the Property and Tax Lot tables
		- **Info button to access Detail view:** To see the detail view of a record, click on the “info” icon on the left side of the tab grid.

		![inventory list change v2.0.0](images/release_notes/2_0_image6.png)

	#### Known Issues

	- **Actions pulldown:** the Actions pulldown does not contain options for creating and adding to existing Projects, as Projects have not been implemented in this version.

	- **Sorting alphanumeric fields does not work properly in all cases ([1218](https://github.com/SEED-platform/seed/issues/1218)):** There are some fields (generally defined as numeric) that the program is not sorting properly when the data is alphanumeric. One example is a Zip Code field that would generally have 5 digits, but in some cases may have 9 digits with a hyphen separating the 5 digit and 4 digit sections.

	- **Some mapped data is not displaying in detail and list view ([1213](https://github.com/SEED-platform/seed/issues/1213)):** Under some circumstances, not all the mapped fields are displayed in the List or Detailed view, and are not available to select in the List Settings for either view. It is therefore important to check in both the Mapping Review screen and the final records in the Inventory lists (Property and Tax Lot) to make sure that all the fields in the original file are displayed. If they are not, it may be necessary to reimport the data and change either the mapping or the field names in the original file. 

	- **Slow display of records for large data sets ([1105](https://github.com/SEED-platform/seed/issues/1105)):** For organizations that have more than a few thousand records in either the Tax Lot or Property tables, the display of the records can take several seconds, because the program is loading all the records into the view. However, once the records are loaded, the actions in the view (filtering, sorting, etc) will be very responsive.

	- **Deleting Records ([1214](https://github.com/SEED-platform/seed/issues/1214)):** Deleting records (from the Actions pulldown list) will delete associated Tax Lot and Property records. If this is not desired, it might be necessary to label the record in question for deletion but not actually delete it in this version of the program. Future versions may include the option to delete the record in question without deleting it’s paired record, and should include the feature to allow un-pairing of records (unmatching “by hand”), which would then allow deletion of the records without deleting the previously paired record. 

	- **Hide Column doesn't persist ([1220](https://github.com/SEED-platform/seed/issues/1220)):** The Hide Column feature doesn't persist the state of hidden columns when moving off the current view. When coming back to that view, the hidden column will no longer be hidden. The work around is to define which columns should be visible in the List view through the List Settings feature. 

		![hide column doesn't persist v2.0.0](images/release_notes/2_0_image7.png)

	### Inventory Detail View

	#### Changes

	- **Default Detail view will not show all fields:** The first time the Tax Lot or Property Detail view is accessed, not all the fields will be displayed. However, using the List Settings allows all the mapped fields to be selected for display (with the exceptions noted in [1213](https://github.com/SEED-platform/seed/issues/1213)).

	#### Known Issues

	- **Import history not displayed ([1139](https://github.com/SEED-platform/seed/issues/1139)) (but edit history is displayed):** The import history for a given record is not being captured or displayed in the Detail view (this history was captured and displayed in V 1.5). However, when a record is edited in the Detail view, the program does keep the history. 

		![import history not displayed v2.0.0](images/release_notes/2_0_image8.png)

	### List Settings

	#### Changes

	- **Field Display status and order:** In List Settings, the functions of selecting which fields to display and setting their order happens in the same screen and does not need to be saved. The last state of the fields is saved automatically. 

	- **Separate List Settings for Tax Lot and Property Detail view:** The program allows a different List Settings “state” for Tax Lot and Property Detail views. 

	#### Known Issues

	- **Property and Tax Lot indicators are not always correct ([1170](https://github.com/SEED-platform/seed/issues/1170)):** In List Settings, the program attempts to indicate whether a field belongs to the Tax Lot or Property table. However, in come circumstances, those indicators are not correct. But these indicators are strictly informational and don't affect the display of the data if the fields are selected

		![incorrect indicators v2.0.0](images/release_notes/2_0_image9.png)

	- **Multiple fields with the same name ([1171](https://github.com/SEED-platform/seed/issues/1171)):** In List Settings, there may be multiple instances of the same field name, possibly with the wrong marker for which table it belongs to, with no indication which will contain data. 

		![multiple fields with same name v2.0.0](images/release_notes/2_0_image10.png)

		Generally, the first one in the list will be the one that will display data. However, if that isn't the case, the work around for this situation is to select all of the fields, go back to the list view, determine which one shows data, and from the list view, use the Hide Column option (accessed from the down arrow in the upper right of the field column) to hide the fields that do not have data.

		![multiple fields with same name image 2 v2.0.0](images/release_notes/2_0_image11.png)

	### Labels

	#### Changes

	- Label Admin is under Organizations: The Label admin screen used to be in the Building list (which is now either Tax Lot or Property) but has been moved in this version to the Organizations view

	### Organizations

	#### Changes

	- **Cycles Admin link added:** Cycles are defined in Organizations

	- **Labels Admin link moved:** The Labels admin link is moved from the old Building list to Organizations

		![labels admin link moved v2.0.0](images/release_notes/2_0_image12.png)

	#### Known Issues

	- **Cycles:** There is currently not an option to delete existing cycles

	### API Documentation

	#### Changes

	- API Documentation in navigation bar: This version has a new option in the main Navigation bar called API DOCUMENTATION, which will display a Swagger API platform which shows how each API is used in the program as well as having the option to test API functionality

		![swagger documentation screenshot v2.0.0](images/release_notes/2_0_image13.png)

	### Administration (Superuser)

	#### Changes

	- **Admin screen:** The list of organizations under the admin screen now shows the Parent ID if there are suborganizations, as well as the internal database organization ID, the date the organization was created, and the Property and Tax Lot record count by Cycle. 

	#### Known Issues

	- **User account without an organization ([1024](https://github.com/SEED-platform/seed/issues/1024)):** The program will allow a superuser to create a user account without an organization, so make sure that all the fields are properly defined, including the organization, when creating new users.

	#### Bug Fixes

	- **Performance enhancements:** It is much faster to view the organizations in the program, as well as to delete records from organizations.

??? note "**Version 1.5.0**"

	## Version 1.5.0

	### Labels

	#### Bug Fixes

	- When adding labels from the Building List, the program generates the list of labels even with large data sets, including selecting records from multiple pages.

	- When you click on the Building Detail view, the program keeps the "filter by label" status at the Building List level. 

	### Data Import

	#### Bug Fixes

	- Program now handles many unusual characters in Excel files, such as bullets, new lines, etc.

	- There have been improvements when importing large files with thousands of records.

	### Building List

	#### Bug Fixes

	- Program stays on the Building List page where you started when returning from Building Detail. If you are on page 10 in the Building List and go to the Building Detail view for one of the records on that page, when you come back to the Building List, you are still on page 10. The program used to put you back on page 1.

	- A single quote (such as apostrophe) no longer causes the building search function to crash

	- Filtering on the date fields should now work for Mozilla Firefox and Microsoft Internet Explorer. For those two browsers, the date format needs to be "2014-12-31".

	### Building Detail

	#### Bug Fixes

	- The field order is no alphabetical by default

	#### Enhancements

	- The program now allows resizing of the columns.

	- Clicking on a field shows the entire contents of the field in a call out.

	### Mapping

	#### Bug Fixes

	- The program shows all the mapped fields in the Mapping screen, including those in the extra_data JSON blob field.

	### Projects

	#### Bug Fixes

	- Exporting records from Projects has been fixed

	### Behind the Scenes

	#### Bug Fixes

	- Many code cleanup changes have been made which allows for more efficient development




