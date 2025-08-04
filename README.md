# PauseAI N8N Automations

This repository is to keep track of how PauseAI does automations, and to have a place to discuss issues.
We used to use Zapier, but migrated to n8n early 2025.

- Instance available on [n8n.pauseai.info](https://n8n.pauseai.info/)
- Discusson on [PauseAI Discord](https://discord.com/channels/1100491867675709580/1384190832562671718/1384190832562671718)

## Instance

- Hosted on DigitalOcean, managed by Joep Meindertsma 

### Upgrading n8n

Log in to [the droplet console](https://cloud.digitalocean.com/droplets/502581104/graphs?i=4e6187&period=hour) and execute these commands: 

```sh
cd /opt/n8n-docker-caddy
docker compose pull
docker compose down
docker compose up -d
```

## Automations

### New Member

On new Airtable Members, create a discord message to the pipeline and add a volunteer role.

_This is disabled, as we use Airtable to send summaries to chapter leads. The volunteer role doesn't work because [we need Discord IDs](https://github.com/PauseAI/n8n-automations/issues/1)._

### Netlify Build

Creates a message on build fails in #software-updates.

