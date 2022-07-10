# Discord Bot - Cloudflare Worker Template
<div align="center">
  <p>
    <a href="https://discord.gg/BTXJmW4Bh7"><img src="https://img.shields.io/discord/395423304112013334?logo=discord&logoColor=white" alt="Discord server" /></a>
    <a href="https://github.com/ssMMiles/discord-interactions/actions"><img src="https://github.com/ssMMiles/interactions.ts/actions/workflows/tests.yml/badge.svg" alt="Tests status" /></a>
  </p>
</div>
*A template Discord bot made using [@discord-interactions](https://github.com/ssMMiles/discord-interactions).*

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/ssMMiles/discord-interactions-worker)

## Getting Started
### Cloning the repo
You can either use degit to locally clone this repo without git, or [create a new repo from this template](https://github.com/ssMMiles/discord-interactions-worker/generate) and clone that.
```sh
npx degit ssMMiles/discord-interactions-worker
```

After that, make sure to install dependencies using npm:
```sh
npm install
```

### Installing and setting up Wrangler
> Make sure to [sign up for a Cloudflare Workers account](https://dash.cloudflare.com/sign-up/workers) in a browser before continuing.
Install wrangler with npm or yarn:
```sh
npm install -D wrangler@latest
# yarn global add wrangler@latest
```
Read more about [installing wrangler](https://developers.cloudflare.com/workers/cli-wrangler/install-update).

Afterwards, run `wrangler login` to login to your Cloudflare account with OAuth:
```sh
wrangler login
```

Copy `wrangler.example.toml` into `wrangler.toml` and edit it as you'd like.

### Filling in secrets
You can enter in environment secrets with `wrangler secret put`, here are the keys that are required to run this:
```sh
npx wrangler secret put CLIENT_ID
npx wrangler secret put PUBLIC_KEY
npx wrangler secret put TOKEN
```

### Development
To run this locally, copy `.dev.vars.example` to `.dev.vars` and fill in the variables, then you can run it through `npm run start`, or `npm run dev` to proxy it through an SSH tunnel to Ngrok.

### Production
To deploy, just use `npm run deploy`.