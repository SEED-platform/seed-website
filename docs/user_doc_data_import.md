[]{#anchor}**Data Import**

SEED is primarily a data management platform, and importing the data is
a critical component to understand.

[]{#anchor-1}**Overview**

SEED can import data from many different sources, for example:

[]{#anchor-2}Building / Property Data

Building and property lists can sometimes be difficult to create. There
are a few different sources of data that may help, which can be imported
into SEED in the form of spreadsheets with one line per building, such
as:

-   Tax assessor lists

-   Real estate data

[]{#anchor-3}Benchmarking data

One of the primary sources of building information for benchmarking and
Building Performance Standards (BPS) ordinances is data entered by
building owners into ENERGY STAR Portfolio Manager which is then shared
with jurisdictions who are determining compliance with the ordinances.

SEED can import data from spreadsheets downloaded from ENERGY STAR
Portfolio Manager and then imported into SEED. It is also possible to
log into an ENERGY STAR Portfolio Manager account directly from SEED and
specify a report to be imported. This functionality is not currently
automated.

[]{#anchor-4}Match data from different sources

One of the strengths of SEED is that data for a specific building or
property can be imported from multiple sources and then matched and
merged within SEED so that all the information related to that building
is collected in one platform.

In order for the data from different sources to be merged together,
there must be one or more "matching" fields that are in all the data.
These fields are identified during the data import "Mapping" step, which
will be discussed in the next section. These matching fields typically
include:

-   Tax Assessor Parcel ID

-   Custom Building ID

-   ENERGY STAR Portfolio Manager ID

[]{#anchor-5}Handle data with different types of relationships

In addition to matching and merging data for the same building or
property, SEED can establish a relationship between a Tax Assessor
Parcel and the buildings or properties associated with that parcel.
Establishing this relationship is optional, but if Tax Assessor Parcel
data is used to begin the creation of a building or property list, or
the parcel / building relationship is desired, SEED can accomplish this
during the mapping process, as long as there is both a tax parcel ID and
a building or property ID in the data being imported.

The image below shows the possibilities of tax parcel and building
relationships:

-   Case A: A one to one relationship, ie, one building on one parcel

-   Case B: Multiple buildings on one parcel

-   Case C: One building on multiple parcels

-   Case D: Multiple buildings on multiple parcels, such as a campus
    > scenario

![](Pictures/10000201000004FE0000028E8C0220C39544F7EF.png){width="9in"
height="4.611in"}

The SEED data model establishes the relationship between the tax parcels
and buildings as shown in the simplified diagram below. In the main
Inventory list view, there are two tabs, one for Property and one for
Tax Lot.

![](Pictures/100002010000042C000002622E2149B077A45A03.png){width="9in"
height="5.139in"}

[]{#anchor-6}Maintain data based on compliance year

Data is imported into SEED by "cycles", which are generally defined on a
calendar basis, to keep track of the annual compliance of buildings.
There are several features in SEED which allow importing, viewing, and
analyzing the status of buildings across cycles.

[]{#anchor-7}Data import workflow

The first three steps in the diagram below shows the workflow when
importing data into SEED

![](Pictures/10000201000001E7000002A7490433ED2CCD09F0.png){width="2.7035in"
height="3.7634in"}

[]{#anchor-8}**Before importing data**

There are a few steps that should be completed before importing data, in
order to have a smooth process.

[]{#anchor-9}Define Cycles in Organizations / Cycles

It is important to create the appropriate cycle to import the data into.
SEED has one "default" cycle that can be used as is, or edited to suit
the first data import. It is also possible to make as many cycles as
needed to import the data.

![](Pictures/10000000000003C000000300DF7045FFA704C4B4.png){width="9.0465in"
height="7.2244in"}

![](Pictures/1000020100000467000002D72AA6B8239D921F4B.png){width="9.0118in"
height="5.8134in"}

[]{#anchor-10}**Data files with multiple years of data**

If a file is to be imported with multiple cycles (years) of data in it,
the appropriate cycles need to be defined before importing the data. For
example, if there is data from 2019, 2020 and 2021 in one file, and that
data is to be associated with the cycle for each year, a cycle for each
of those years needs to be defined. SEED uses a field called "Year
Ending". This is a default field that is in ENERGY STAR Portfolio
Manager data, but could be added to other data if needed.

![](Pictures/1000020100000424000000DCE6BBEE8E49512ECD.png){width="8.7134in"
height="1.8083in"}

![](Pictures/1000020100000426000000DC938DECFEC455A3A9.png){width="8.802in"
height="1.8236in"}

Make sure that a cycle is defined for each year of data in the data
file.

![](Pictures/10000201000001CA00000113FCE2346A094CA375.png){width="4.0256in"
height="2.422in"}

[]{#anchor-11}Define Matching fields in Organizations / Column Settings

In order to map the fields properly when importing data, it is important
to define the fields that will be the "matching" fields across data
files.

The matching fields are defined in Organizations / Column Settings.
There is a column called "MATCH CRITERIA", and the fields that are
matching fields should be checked. There can be just one field defined,
or multiple fields. Standard fields for matching are the PM Property ID
field from ENERGY STAR Portfolio Manager, and/or the Custom ID 1 field,
which can represent any unique building ID.

The Column Description field can be edited to represent a more
descriptive name. For example, if the matching field is Custom ID 1,
that Column Description could be changed to "City X Building ID".

![](Pictures/100002010000046E0000025E674835DD2C5BCBEA.png){width="11.8126in"
height="6.3126in"}

Once the cycles are properly defined and the matching fields are set, it
is time to import the data

[]{#anchor-12}**Importing data**

There are a few different ways to start importing data. You can click
the DATA navigation button on the left side of the screen, or you can
click on the "Upload your Buildings List" button on the main SEED
Platform screen.

![](Pictures/1000020100000427000002AEE8B6D4AA8516B312.png){width="8.7547in"
height="5.6453in"}

[]{#anchor-13}Create a data set

The DATA navigation button on the left side of the application will
display the screen shown below, where a new data set can be created. The
Data Set Name can be any text that describes the data set that is being
created. There will potentially be multiple files imported in a data
set.

![](Pictures/1000020100000430000001FA1E06280B8E5E3437.png){width="8.6819in"
height="4.0953in"}

Clicking the "Create Data Set" button will open the screen shown below,
which has several options for what type of data to upload, as well as
how to upload it.

The first step is to assign this data upload to a cycle \-- the pull
down list will show all the cycles that are defined. It is also possible
to define a new cycle by clicking the "Manage available cycles" link
under the Cycle pulldown. And if the file being imported has multiple
years defined (based on a field called "Year Ending") the "Multiple
Cycle Upload" box can be checked.

![](Pictures/10000201000002720000023129FB916B35CD8CDE.png){width="5.5673in"
height="4.9898in"}

[]{#anchor-14}Upload a Spreadsheet

The first option in the list of upload options is "Upload a
Spreadsheet".

This option assumes that the spreadsheet will have one record per
property or tax parcel. This spreadsheet can contain both property /
building and tax parcel information, or it can be just one or the other.

Here is an example of a spreadsheet representing a list of tax parcels
that have buildings on them. Each row represents a tax parcel.

![](Pictures/10000201000002E4000000FF387DF2D534DABD1E.png){width="6.1252in"
height="2.1102in"}

Here is an example spreadsheet of building information from ENERGY STAR
Portfolio Manager for the same buildings. In this case, each row
represents an individual building, and each row has the tax parcel ID
associated with the building.

![](Pictures/10000201000004C60000011AD68131AECF50383C.png){width="10.3366in"
height="2.3846in"}

When these two spreadsheets are imported into SEED, the relationship
between the tax lots and buildings can be established in the mapping
step.

[]{#anchor-15}**Upload a tax parcel spreadsheet**

First, import the tax parcel spreadsheet into the data set by clicking
the Upload a Spreadsheet button, navigating to the file to be imported,
and as the file is imported, messages will appear to show the progress
of the upload.

![](Pictures/1000020100000277000000E28911788AFD7C935A.png){width="5.5681in"
height="1.9937in"}

This message appears when the file has completed the first upload step.
Click the "Continue to data mapping" button to move to the next step.

![](Pictures/100002010000027F00000110432629A458833B78.png){width="5.9374in"
height="2.528in"}

[]{#anchor-16}Mapping the data

The Mapping screen will now appear, and the fields in the uploaded file
need to be mapped to the appropriate SEED fields.

If this is the first file being imported, the easiest way to start the
mapping is to click the "Copy Data File Headers directly to SEED
headers" which copies the fields from the right hand side (the fields in
the uploaded file) to the SEED Mapped Fields on the left side.

![](Pictures/1000020100000529000002B7A106E2E02F83BAD3.png){width="10.5516in"
height="5.5516in"}

Change the field called "Parcel Number" to the matching field
"Jurisdiction Tax Lot ID".

![](Pictures/100002010000024D000000760076AACC8D567D9A.png){width="5.1925in"
height="1.0402in"}

Save the final mapping to a "Column Mapping Profile name, to save the
mappings for another file of the same structure.

![](Pictures/10000201000002CF000000FA39E2413EE461581D.png){width="5.7929in"
height="2.0146in"}

This creates a Column Mapping profile that can be used again for another
file with the same fields.

![](Pictures/10000201000002D600000038C9A84C4A6CFD7AEB.png){width="6.4953in"
height="0.5008in"}

Then click the Map Your Data button to go to the Mapping Review screen.

![](Pictures/100002010000007A0000002EA60B6B8BD58F7671.png){width="1.2728in"
height="0.4799in"}

[]{#anchor-17}Review the mapped data

In the Mapping Review screen all the records will be displayed, with the
new field mapping. If there is anything that needs to be changed, click
the Back to Mapping button and the mapping can be changed as needed.

![](Pictures/10000201000004B000000242270A1289EC66D1C3.png){width="9.7217in"
height="4.6819in"}

Click the Save Mappings button to complete the data upload process; a
confirmation screen will be displayed. Click the Confirm mappings

![](Pictures/100002010000024700000126B4E2620623B03342.png){width="5.5256in"
height="2.7866in"}

A progress bar will be displayed.

![](Pictures/1000020100000249000000E897650DFC5E419893.png){width="5.328in"
height="2.1134in"}

When the matching is complete, a summary of what was imported will be
displayed.

![](Pictures/1000020100000249000001C1A958A4A27ADBA30E.png){width="5.6311in"
height="4.322in"}

Click the View my Properties to go to the Inventory list to see the
uploaded data.

[]{#anchor-18}Importing ENERGY STAR Portfolio Manager Data

There are two methods for importing ENERGY STAR Portfolio Manager Data

-   Download a spreadsheet from the ENERGY STAR Portfolio Manager
    > application and import that spreadsheet into SEED

-   Log in to the ENERGY STAR Portfolio Manager account from SEED and
    > specify the Custom Report Template to upload into SEED. This
    > eliminates the need to use the spreadsheet option

![](Pictures/1000020100000398000002DB4E73C53A6A1B80F1.png){width="7.7366in"
height="6.1472in"}

[]{#anchor-19}**Upload an ENERGY STAR Portfolio Manager spreadsheet**

After uploading the tax lot spreadsheet, the next step might be to load
the ENERGY STAR Portfolio Manager spreadsheet for the buildings
associated with the tax lots already imported.

The same steps are followed as any other spreadsheet:

-   In the same Data Set, click the Add more data files link

> ![](Pictures/100002010000035E000000AC4AD160CA0058738E.png){width="7.089in"
> height="1.4146in"}

-   Make sure the same cycle is selected, then click the Upload a
    > Spreadsheet button.

> ![](Pictures/1000020100000219000000DE657C8657B2597781.png){width="4.8902in"
> height="2.0217in"}

-   Browse to the appropriate file

-   In the Mapping screen

    -   Copy the Data File headers to the SEED headers

    -   Set the INVENTORY TYPE to Property for all fields except "Parcel
        > ID"

    -   Set the INVENTORY TYPE to Tax Lot for the "Parcel ID" field, and
        > change the SEED Header mapping to the Tax Lot matching field
        > "Jurisdiction Tax Lot ID". This will establish the
        > relationship between the PM Property ID Matching field and the
        > Jurisdiction Tax Lot field for each record

    -   Save the final mapping to a new Column Mapping Profile

    -   Click Map Your data to go to the Mapping Review screen

> ![](Pictures/10000201000004080000024703F8BB09F928946C.png){width="8.5256in"
> height="4.8126in"}

> Mapping the Parcel ID to the Tax Lot table and the PM Property ID to
> the Property table results in records where the data from each can be
> viewed together.

> ![](Pictures/10000201000003BB000002732CB63029B45A0E3D.png){width="8.6925in"
> height="5.6917in"}

-   The Mapping Review screen will show the records mapped to the
    > Properties table and the records mapped to the Tax Lot table

> ![](Pictures/10000201000004250000035EE23EA55F97C5B662.png){width="9.602in"
> height="7.8016in"}

-   Click Save Mappings to finish the record mapping and matching
    > process

    -   The progress bar will be displayed

> ![](Pictures/1000020100000246000000DC14514783BBAEE863.png){width="5.5256in"
> height="2.089in"}

-   -   The results of the matching and merging will be displayed

> ![](Pictures/10000201000002490000015DA53158BBBA759A2E.png){width="5.6402in"
> height="3.3654in"}

-   Click the View my properties button to view the imported data in the
    > Inventory List

> ![](Pictures/10000201000004BF000001D81A6894FC88393AA5.png){width="9.911in"
> height="3.8508in"}

[]{#anchor-20}Adding Meter Data

[]{#anchor-21}Adding Sensor Data

[]{#anchor-22}Deleting Data and Data Sets
