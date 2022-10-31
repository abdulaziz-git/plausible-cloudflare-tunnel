# Plausible Analytics setup examples with Cloudflare Tunnel from Cloudflare Zero Trust

This repository acts as a template to get up and running with [Plausible Analytics](https://github.com/plausible/analytics). with cloudflare tunnel.

### How to use

Find instructions on how to run Plausible Analytics Self Hosted [in our docs](https://plausible.io/docs/self-hosting).
Make sure you have cloudflare account with domain added and already sign up for Cloudflare Zero Trust.
1. Go to [cloudflare zero trust dasboard](https://dash.teams.cloudflare.com/)
2. Create new tunnel by go to __Access__ > __Tunnel__ > __Create Tunnel__, give your tunnel a name for example, __tunnel-VPC-01__
3. Copy tunnel token and paste in __.env__ file (**CLOUDFLARED_TOKEN=yourtunneltoken**)
4. Start plausible with docker compose
```bash
docker-compose up -d
```
5. Still in tunnel page, create __Public Hostname__, select __Subdomain (optional)__ and __Domain__ and make sure to choose Service Type __HTTP__ and URL __plausible:8000__
6. Go to https://yourdomain

### Contributing

We are always looking to expand on the options and setups provided here. Feel free to open an issue or PR if you feel
something could be improved.

### Upgrade guides

- [Upgrading `plausible_db` (PostgreSQL)](upgrade/postgres.md)
