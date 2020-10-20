# FAQ - Hosting

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
	See the [Technical Allies page](../technical_ally.md) for more information.

Options (1) and (2) are highly dependent on internal expertise and potential requirements related to sharing outside of a user's organization. Generally, cloud hosting simplifies management of networks, hardware, firewalls, and backups. An example SEED instance hosted in the cloud with staging and production environments costs approximately $1,000 to $1,500 per month for a large instance capable of processing records for an entire region.
