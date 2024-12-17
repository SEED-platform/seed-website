# About

## Hosting Options

SEED is a web-based database tool, and therefore must be "hosted" on a web server. It is not designed to be installed on an end-user's desktop computer. There are several options for how SEED can be hosted. The following information will help you select an appropriate type of SEED instance.

If you are a developer, consult the [Developer Getting Started Guide](https://seed-platform.readthedocs.io/en/latest/getting_started.html) for detailed instructions on how to install the SEED Platform locally for development purposes.

### Third-Party Hosting

SEED can be hosted by third-party hosting providers, who will provide access to a SEED account. Approved providers are responsible for keeping up with the updates to the code. See the [Technical Allies](technical_ally.md) page for current hosting providers.

### Self-Hosted

Organizations may want to host their own SEED installation, either on user-owned hardware or on the cloud (e.g. Amazon, Google Compute). This requires the SEED source code, installation scripts, and installation instructions, all of which are available on GitHub. Note that SEED is a server-based web application that is not designed to be installed on an end-user's desktop computer. Self-hosting SEED requires some experience with server and database administration and will usually require the involvement of an organization's IT department for installation and operation of a SEED instance. For more information on self-hosting, see the [self-hosting](self_hosting.md) page.

### DOE/National Lab-Hosted Instance

#### SEED Account Request

We can provide a SEED account on the DOE/National Lab-Hosted SEED Platform for jurisdictions or organizations that are exploring or in the process of implementing a Building Energy Benchmarking or Building Performance Standard ordinance. Please [inquire here](https://buildingdata.energy.gov/#/help-desk) and select SEED as the relevant tool to start a discussion with us about this possibility.

#### Hosting Terms of Service

DOE and the National Laboratories agree to provide:

- Improvements to the SEED Platform features based on partner input and priorities.

- Business process support to help optimize organizational data management, software integration, and data quality.

- Technical Assistance with initial account set-up and load, combine, and map data sets to assemble your master buildings list; determine compliance with your program requirements; provide technical guidance and support on establishing API connections with related applications such as third-party CRM applications.

- Hosting services for your SEED account.

#### Data Privacy Policy

You, and your company or organization (the PROVIDER) have agreed to upload and provide PROPRIETARY DATA, including energy efficiency data, building data, and building energy performance data to the Standard Energy Efficiency Data (SEED™) Platform database that the U.S. Department of Energy (the Government) and Alliance for Sustainable Energy, LLC (“Alliance”) the manager and operator of the National Renewable Energy Laboratory (“NREL”) (the RECIPIENT) have created and provide for use for registered users.

PROPRIETARY DATA is defined as follows:

(a) information that embody trade secrets or commercial or financial information that is confidential and privileged;

(b) information that is confidential and privileged and developed at private expense (i.e., not with Federal funds);

(c) information that is not customarily released to the public; and/or

(d) information whose disclosure to the public could result in financial harm to the PROVIDER, to owners of buildings whose information is contained in the  PROPRIETARY DATA, or to other stakeholders.

In order to upload PROPRIETARY DATA, you will be required to create an account and provide the RECIPIENT with a username, password, and email address. You are solely responsible for maintaining the confidentiality of the password and username you provided during the registration process and are fully responsible for all activities that occur under your password or account.

The PROPRIETARY DATA shall remain protected until the PROVIDER provides notice of termination of their account on the SEED Platform and provides notice to remove PROPRIETARY DATA from the SEED Platform database, at which time the RECIPIENT will promptly return and/or destroy the PROPRIETARY DATA uploaded in the SEED Platform database.

By providing the PROPRIETARY DATA, PROVIDER agrees to the following:

- PROVIDER has the authority to provide the PROPRIETARY DATA to the RECIPIENT, that the information provided constitutes PROPRIETARY DATA, and consents to the information provided being labeled and treated as PROPRIETARY DATA. If PROVIDER wishes to provide non-proprietary data, please contact <BTODataTools@ee.doe.gov>.

- RECIPIENT may host, display, and manage such PROPRIETARY DATA for the PROVIDER and the Government to access, analyze, and manage through the SEED Platform.

- RECIPIENT may use, view, or duplicate the PROPRIETARY DATA and may share the PROPRIETARY DATA with support services contractors within the scope of their contracts. RECIPIENT may share the PROPRIETARY DATA to other DOE National Laboratories participating in the SEED Platform project, under the restriction that (i) the PROPRIETARY DATA be retained in confidence and not be further disclosed, (ii) the PROPRIETARY DATA will be destroyed when the DOE National Laboratory’s participation in the SEED Platform has ended.

Download a copy of the [data privacy policy](resources/SEED Data Privacy Terms.pdf).

Please [contact us](contact.md) if you have any questions about this privacy policy. Any data uploaded to National Lab hosted SEED instances or shared with NREL/LBNL is proprietary and not to be shared.

#### Data Security

The National Renewable Energy Laboratory and Lawrence Berkeley National Laboratory (LBNL) have implemented a number of software and security controls to ensure the security of data stored in the SEED Platform&trade; software.

SEED Platform&trade; is secured behind the Amazon Web Services (AWS) firewall, and other security measures are in place as well. For more information about specific security protocols, please contact us using the information found on the [contact page](contact.md).

## Additional Hosting-Related Questions

### Can the web interface of a self-hosted SEED instance be accessed via a local network, or is internet access required? Can access via local internet be disabled?

Access via public internet would be a function of the self-hosted instance's network configuration. If SEED is hosted on Amazon Web Services, for example, the host can deny access based on CIDR blocks (IP address ranges) in the Amazon Web Services Console. If the application is hosted on user-owned infrastructure, a local firewall can prevent external access. Note that internal access in both cases would still be available (i.e., the web interface would be accessible).

### What is the estimated cost to implement and maintain the SEED Platform?

There are three hosting options:

1. Self-hosting on user-owned hardware
2. Self-hosting on the cloud (e.g. Amazon, Google Compute)
3. Paying a hosting provider. Several companies offer SEED as a hosted solution:

    - [ClearlyEnergy](https://www.clearlyenergy.com/)
    - [Earth Advantage](https://www.earthadvantage.org/creating-change/home-energy-score.html)
    - [Open](https://opentech.eco/)
    - [PSD Consulting](http://psdconsulting.com)

4. DOE/National Lab-Hosted Instance

See the [Technical Allies page](technical_ally.md) for more information.

Options (1) and (2) are highly dependent on internal expertise and potential requirements related to sharing outside of a user's organization. Generally, cloud hosting simplifies management of networks, hardware, firewalls, and backups. An example SEED instance hosted in the cloud with staging and production environments costs approximately $1,000 to $1,500 per month for a large instance capable of processing records for an entire region.
