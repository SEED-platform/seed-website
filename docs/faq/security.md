# FAQ - Security

## Can you suggest any encryption solutions, since the SEED software does not encrypt its database?

We recommend hard drive encryption of the database server as the easiest solution; encrypting locally is more complicated but certainly doable.

## How does SEED secure internet data communications?

Secure sockets layer (SSL) protocols must be configured on the hosted instance. This requires purchasing and adding certificates to the deployed server, or using a third-party service (e.g. CloudFlare or Cloudfront) to manage the domain name system (DNS) and the SSL certificates.
