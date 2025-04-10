# April 10 2025

Auvik is aware of this repo, this will no longer function to get billable devices for a promo.  Leaving the repo up for folks to experiment with.

# Auvik Collector

Simple repo for spinning up auvik collector and handful of dummy managed devices.

The dummy devices use pfsense as the snmpd description as this tricks Auvik into thinking they are firewalls. 

## Deployment

1. Update docker-compose with Auvik Creds
1. Update snmpd.conf.template with domain, purely for cosmetic reasons
1. Deploy

```
docker-compose up -d
```

## Scale Devices

If you want to scale up dummy devices:
```
docker-compose up -d --scale pfsense=5
```
