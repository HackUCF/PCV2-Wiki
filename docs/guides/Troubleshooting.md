# Troubleshooting

This page provides methods for troubleshooting problems the end user may run into.

## Hackucf DNS records not resolving:

## Recommended Fix
  Set your DNS to cloudflare's dns servers. Follow the instructions [located on their website](https://one.one.one.one/dns/)

### Fix for Custom DNS Users

   If you run your own local DNS and you cannot resolve horizon.hackucf.cloud with nslookup, then you will need to add the following to your Records.

   **DNS Records:**

   | Domain         | IP Address |
   |----------------|------------|
   | cloud.hackucf  | 10.4.4.10  |

   **CNAME Records:**

   | FQDN                | Domain        |
   |---------------------|---------------|
   | horizon.hackucf.cloud | cloud.hackucf |
   | api.hackucf.cloud     | cloud.hackucf |
