# Frequently Asked Questions

## How can I get information on capabilities, summary of features, and current development of SEED?

* For a list of new features and fixed capabilities, visit the [SEED Platform GitHub Releases](https://github.com/SEED-platform/seed/releases) page.

* Consult the [Reference Page](references.md) for publications related to SEED. Additionally, the following paper describes the BuildingSync® format which can be used to import data into the SEED Platform:
	* DeGraw, Jason, Kristin Field-Macumber, Nicholas Long, and Supriya Goel. 2018. [“BuildingSync® in Action : Example Implementations.”](https://buildingsync.net/documents/DeGraw-ACEEE-BuildingSync-in-Action.pdf) In 2018 ACEEE Summer Study on Energy Efficiency in Buildings, 1–12. Pacific Grove, CA.

* The following is a list of related projects that are using the SEED Platform:
	* [OEP Project](http://psdconsulting.com/openefficiency-platform/)
	* [BRICR Project](https://aceee.org/files/proceedings/2018/#/paper/event-data/p110) and [BRICR Presentation](https://www.energy.gov/sites/prod/files/2018/05/f52/24293_Hooper_050318-900.pdf)
	* [EDV Project](https://www.energy.gov/eere/buildings/energy-data-vault)


## If a SEED Platform instance is self-hosted, could the web interface be accessed within a local network, or must the database be accessed through the internet? Can access through the public internet be disabled?

Access to the public internet would be a function on how the networking is configured on the self-hosted instance. If SEED is hosted on Amazon Web Services (as an example), then the host can block access based on CIDR blocks (IP address ranges) in the Amazon Web Services Console. If the application is hosted on user-owned infrastructure, then a local firewall could be setup to prevent external access. Note that internal access in both cases would still be available (i.e., the web interface would be accessible).

## What is the estimated cost to implement and maintain the SEED Platform as part of a benchmarking system? 

There are three options for hosting:

1. Self hosting on user owned hardware
2. Self hosting on cloud resources (e.g., Amazon, Google Compute, etc.).  
3. Paying a hosting provider. Some companies are offering SEED as a hosted solution:
	* [ClearlyEnergy](https://www.clearlyenergy.com/)
	* [Earth Advantage](https://www.earthadvantage.org/creating-change/home-energy-score.html)
	* [Open](https://opentech.eco/)
	* [PSD Consulting](http://psdconsulting.com) 
	See the [Technical Allies page](technical_ally.md) for more information.

Options (1) and (2) are highly dependent on internal expertise and potential requirements related to sharing outside of a user's organization. In general, hosting on a cloud resource gives the user the ability to more easily manage the network, hardware, firewalls, and backups. An example SEED instance hosted in the cloud with staging and production environment costs approximately $1,000-$1,500/month in hosting for a relatively large instance that can process records for an entire region.

## Can you suggest any alternative methods to encrypt the SEED database, since the SEED software does not encrypt its database? 

The easiest solution would be to encrypt the hard drive of the database server. This is as simple as clicking a button on cloud resources. Locally, it is a bit more complicated, but definitely doable.

## How does SEED secure data communications over the internet?

SSL must be configured on the hosted instance. This can be accomplished by purchasing certificates and adding them to the deployed server or using a third party service (e.g., CloudFlare, CloudFront, etc.) to manage DNS and the SSL certificates.

## What resources or support do you provide to jurisdictions who wish to implement the SEED Platform for a benchmarking program?

We typically provide technical support within reason as needed. As the community grows, there are more users that are able to provide support. It is recommended to use [GitHub issues](https://github.com/SEED-platform/seed/issues) to a) view existing feature requests and issues, and b) communicate with various developers.

## Are there any organizations that are developing free and open-source plug-ins for SEED? 

You can find more information about organizations contributing to the SEED Platform development below:

* [SEED Platform Collaborative](https://www.energy.gov/eere/buildings/seed-platform-collaborative)
* [SEED Platform Contributing Developers](https://github.com/SEED-platform/seed/blob/develop/AUTHORS.md)
* [SEED Technical Allies](http://seedinfo.lbl.gov/SEED-Technical-Allies)
* [Open Efficiency Platform](https://github.com/OpenEfficiencyPlatform/OEP)
* [BRICR](https://www.energy.gov/sites/prod/files/2018/05/f52/24293_Hooper_050318-900.pdf)
* [EDV](https://www.energy.gov/eere/buildings/energy-data-vault)

## Do you anticipate any SEED issues if there are irregular data updates for each building? For example, with a point-of-sale benchmarking program, building data would only be updated when a property is sold.
	
There should not be any issues importing data at non-regular times. Users do that all the time with the Energy Star Portfolio Manager data.

## Do any applications use SEED to store and analyze building construction permit applications for energy code compliance? 

We are not aware of any applications using SEED for this specific use case, although SEED could be linked to another tool like SalesForce.  We recommend reaching out to Earth Advantage and Clearly Energy for more details (see the [technical allies page](technical_ally.md)).


