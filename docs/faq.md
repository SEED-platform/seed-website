# Frequently Asked Questions

## How can I get information about the capabilities, features, and active development of SEED?

* For a list of new features and fixed capabilities, visit the [SEED Platform GitHub Releases](https://github.com/SEED-platform/seed/releases) page.

* Consult the [Reference Page](references.md) for publications related to SEED. Additionally, this paper describes the BuildingSync® format which can be used to import data into the SEED Platform:
	* DeGraw, Jason, Kristin Field-Macumber, Nicholas Long, and Supriya Goel. 2018. [“BuildingSync® in Action : Example Implementations.”](https://buildingsync.net/documents/DeGraw-ACEEE-BuildingSync-in-Action.pdf) In 2018 ACEEE Summer Study on Energy Efficiency in Buildings, 1–12. Pacific Grove, CA.

* Here are some related projects that are using SEED:
	* [The OpenEfficiency Platform (OEP) Project](http://psdconsulting.com/openefficiency-platform/)
	* [The BayREN Integrated Commercial Retrofits (BRICR) Project](https://aceee.org/files/proceedings/2018/#/paper/event-data/p110) and [BRICR Presentation](https://www.energy.gov/sites/prod/files/2018/05/f52/24293_Hooper_050318-900.pdf)
	* [The Energy Data Vault (EDV) Project](https://www.energy.gov/eere/buildings/energy-data-vault)


## Can the web interface of a self-hosted SEED instance be accessed via a local network, or is internet access required? Can access via local internet be disabled?

Access via public internet would be a function of the self-hosted instance's network configuration. If SEED is hosted on Amazon Web Services, for example, the host can deny access based on CIDR blocks (IP address ranges) in the Amazon Web Services Console. If the application is hosted on user-owned infrastructure, a local firewall can prevent external access. Note that internal access in both cases would still be available (i.e., the web interface would be accessible).

## What is the estimated cost to implement and maintain the SEED Platform as part of a benchmarking system? 

There are three hosting options:

1. Self-hosting on user-owned hardware
2. Self-hosting on the cloud (e.g. Amazon, Google Compute)
3. Paying a hosting provider. Several companies offer SEED as a hosted solution:
	* [ClearlyEnergy](https://www.clearlyenergy.com/)
	* [Earth Advantage](https://www.earthadvantage.org/creating-change/home-energy-score.html)
	* [Open](https://opentech.eco/)
	* [PSD Consulting](http://psdconsulting.com) 
	See the [Technical Allies page](technical_ally.md) for more information.

Options (1) and (2) are highly dependent on internal expertise and potential requirements related to sharing outside of a user's organization. Generally, coud hosting simplifies management of networks, hardware, firewalls, and backups. An example SEED instance hosted in the cloud with staging and production environments costs approximately $1,000 to $1,500 per month for a large instance capable of processing records for an entire region. 

## Can you suggest any encryption solutions, since the SEED software does not encrypt its database? 

We recommend hard drive encryption of the database server as the easiest solution; encrypting locally is more complicated but certainly doable. 

## How does SEED secure internet data communications?

Secure sockets layer (SSL) protocols must be configured on the hosted instance. This requires purchasing and adding certificates to the deployed server, or using a third-party service (e.g. CloudFlare or Cloudfront) to manage the domain name system (DNS) and the SSL certificates. 

## What resources or support do you provide to jurisdictions interested in using SEED as part of a benchmarking program?

We typically provide technical support within reason as needed. As the community grows, there are more users able to provide support. It is recommended to use [GitHub issues](https://github.com/SEED-platform/seed/issues) to a) view existing feature requests and issues, and b) communicate with various developers.

## Are there any organizations that are developing free and open-source plug-ins for SEED? 

You can find more information about organizations contributing to SEED Platform development below:

* [SEED Platform Collaborative](https://www.energy.gov/eere/buildings/seed-platform-collaborative)
* [SEED Platform Contributing Developers](https://github.com/SEED-platform/seed/blob/develop/AUTHORS.md)
* [SEED Technical Allies](http://seedinfo.lbl.gov/SEED-Technical-Allies)
* [Open Efficiency Platform](https://github.com/OpenEfficiencyPlatform/OEP)
* [BayREN Integrated Commercial Retrofits (BRICR)](https://www.energy.gov/sites/prod/files/2018/05/f52/24293_Hooper_050318-900.pdf)
* [Energy Data Vault (EDV)](https://www.energy.gov/eere/buildings/energy-data-vault)

## Do you anticipate any SEED issues if there are irregular data updates for each building? For example, with a point-of-sale benchmarking program, building data would only be updated when a property is sold. 
	
There should not be any issues importing data at non-regular times; users frequently do so with ENERGY STAR Portfolio Manager data. 

## Do any applications use SEED to store and analyze building construction permit applications for energy code compliance? 

We are not aware of any applications which use SEED to do this, although SEED could be linked to another tool, like SalesForce.  We recommend contacting Earth Advantage and Clearly Energy for more details (see the [technical allies page](technical_ally.md)).


