# Getting Started

## Installation

SEED Platform is a web-based database tool, and therefore must be "hosted" on a web server. It is not designed to be installed on an end-user's desktop computer. There are several options for how SEED can be "hosted".  The following information will help you select a SEED Platform instance.

### Third-party hosting

SEED can be hosted by third party hosting providers who will provide access to a SEED account. Providers will be LBNL-approved and will be responsible with keeping up with the updates to the code. See the Technical Allies page for current hosting providers.

### Self hosted

Many organizations that are interested in using SEED may want to host their own installation of SEED. This requires the SEED source code, installation scripts, and installation instructions, all available in GitHub. Note that SEED is a server-based web application that is not designed to be installed on an end-user's desktop computer. Self-hosting of SEED requires some experience with server and database administration, and will usually require the involvement of an organization's IT department for installation and operation of an instance of SEED Platform.

### Temporary test account through LBNL

We are currently open to generating temporary test accounts for state and local governments, and/or their relevant service providers that are exploring or in the process of implementing a building energy benchmarking ordinance. For more information, visit the [LBNL SEED Platform](lbnl.md) page.

If you are a developer, consult the [Developer Getting Started Guide](https://seed-platform.readthedocs.io/en/latest/getting_started.html) for detailed instructions on how to install the SEED Platform locally for development purposes.

## Data Guides

The following guides will help familiarize yourself with the types of data that can be imported into the SEED Platform as well as the import process.

| Version | Date | Description |
|---------|------|-------------|
| [2.6.0](https://docs.google.com/a/lbl.gov/viewer?a=v&pid=sites&srcid=bGJsLmdvdnxzZWVkfGd4OjJiZjVmMTliYjg1YTc2YzE) | 08/09/2019 | Overview of the new Meter Data features added to SEED release 2.6.0 |
| [2.4.0](https://docs.google.com/a/lbl.gov/viewer?a=v&pid=sites&srcid=bGJsLmdvdnxzZWVkfGd4OjNhYzRkMWE2NDVmYTgyZjA) | 10/05/2018 | Overview of the main features in the program, with the basic steps to get started |

## Sample Data

Download the [SEED Sample Data zip](http://seedinfo.lbl.gov/getting-started/seed-sample-data.zip?attredirects=0&d=1), which contains two sample data files:

- **covered-buildings-sample.csv**&mdash;sample tax assessor data with 512 building records
- **portfolio-manager-sample.csv**&mdash;sample Energy Star Portfolio Manager data with 512 records which match the data in covered-buildings-sample.csv based on the Address field

This is clearly the "ideal" case, but it is a good set of test data to make sure that the program is performing properly.

See the [user documentation](documentation.md) page for more information on importing data.