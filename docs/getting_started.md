# Getting Started

## Installation

SEED is a web-based database tool, and therefore must be "hosted" on a web server. It is not designed to be installed on an end-user's desktop computer. There are several options for how SEED can be hosted. The following information will help you select an appropriate type of SEED instance.

If you are a developer, consult the [Developer Getting Started Guide](https://seed-platform.readthedocs.io/en/latest/getting_started.html) for detailed instructions on how to install the SEED Platform locally for development purposes.

### Third-Party Hosting

SEED can be hosted by third-party hosting providers, who will provide access to a SEED account. Providers will be approved and will be responsible for keeping up with the updates to the code. See the Technical Allies page for current hosting providers.

### Self-Hosted

Organizations may want to host their own SEED installation. This requires the SEED source code, installation scripts, and installation instructions, all of which are available in GitHub. Note that SEED is a server-based web application that is not designed to be installed on an end-user's desktop computer. Self-hosting SEED requires some experience with server and database administration and will usually require the involvement of an organization's IT department for installation and operation of a SEED instance.

### Temporary Test Account

We are currently open to creating temporary test accounts for state and local governments and/or their relevant service providers that are exploring or in the process of implementing a building energy benchmarking ordinance. For more information, visit the [requesting test Instance](test_instance_request.md) page.

## Data Guides

The following guides detail the SEED import process and supported data types:

| Version | Date | Description |
|---------|------|-------------|
| [2.18.0](resources/SEED Platform V2_18_0 Getting Started Guide.pdf) | 05/01/2023 | Getting Started Guide |
| [2.12.0](resources/SEED Platform V2_12_Analyses.pdf) | 10/18/2021 | Analyses Documentation |
| [2.6.1](resources/SEED Platform V2_6_1 Patch_ Mapping and Merging.pdf) | 01/16/2020 | Mapping and merging data overview | 
| [2.6.0](resources/SEED Platform V2_6_ Meter Data.pdf) | 08/09/2019 | Overview of the new Meter Data features added to SEED release 2.6.0 |
| [2.5.1](resources/SEED%20Platform%20V2_5_%20GIS%20Features.pdf) | 08/26/2019 | Overview of the GIS functionality available in SEED | 

## Sample Data

The SEED Sample Data collection includes two files and can be downloaded from the table below:

- **covered-buildings-sample.csv**&mdash;sample tax assessor data with 512 building records
- **portfolio-manager-sample.csv**&mdash;sample Energy Star Portfolio Manager data with 512 records which match the data in covered-buildings-sample.csv based on the Address field

Note that this represents an ideal case, but it can be used to confirm proper program performance.

All sample data should work with all versions of SEED, although the newer datasets may contain fields that do not exist in earlier versions. 

| Version | Files |
|---------|-------|
| 2.7.0-Beta | [Covered Buildings Sample File](https://raw.githubusercontent.com/SEED-platform/seed/v2.7.0-Beta/seed/tests/data/covered-buildings-sample.csv) &nbsp; &nbsp; [Portfolio Manager Sample File](https://raw.githubusercontent.com/SEED-platform/seed/v2.7.0-Beta/seed/tests/data/portfolio-manager-sample.csv) | 
| 2.6.1 | [Covered Buildings Sample File](https://raw.githubusercontent.com/SEED-platform/seed/v2.6.1/seed/tests/data/covered-buildings-sample.csv) &nbsp; &nbsp; [Portfolio Manager Sample File](https://raw.githubusercontent.com/SEED-platform/seed/v2.6.1/seed/tests/data/portfolio-manager-sample.csv) | 


See the [user documentation](documentation.md) page for more information on importing data.