# ThunderID Node.js Quickstart

A minimal plain Node.js HTTP server demonstrating sign-in and sign-out with the ThunderID JavaScript SDK (`@thunderid/node`). No framework dependencies — just the built-in `http` module.

## Prerequisites

- Node.js 18+
- A running ThunderID instance (default: `https://localhost:8090`)
- A configured application with `http://localhost:3000/callback` added as an authorized redirect URI (see [Import ThunderID Resources](#import-thunderid-resources) below)

## Import ThunderID Resources

This sample ships with a `thunderid-config/` directory containing a declarative YAML file that creates the required user type and application in one step.

1. Open `thunderid-config/thunderid.env` and set your preferred values:
   ```bash
   NODE_QUICKSTART_CLIENT_ID=NODE_QUICKSTART
   NODE_QUICKSTART_CLIENT_SECRET=<a strong secret>
   NODE_QUICKSTART_REDIRECT_URIS=["http://localhost:3000/callback"]
   ```
2. Import via the ThunderID Console (https://localhost:8090/console):
   - **First-time login**: a welcome screen appears with an **Open** button to upload the YAML file directly.
   - **Later**: access the same welcome screen from the user profile menu in the top-right corner of the console.

This creates the `Customer` user type and the `nodejs-quickstart` application under the default organization unit.

## Getting started

1. Copy the environment file and fill in your values:
   ```sh
   cp .env.example .env
   ```

2. Edit `.env` with the credentials you set in `thunderid-config/thunderid.env`:
   ```
   THUNDERID_CLIENT_ID=NODE_QUICKSTART
   THUNDERID_CLIENT_SECRET=<the NODE_QUICKSTART_CLIENT_SECRET value>
   THUNDERID_BASE_URL=https://localhost:8090
   ```

3. Install dependencies and start the server:
   ```sh
   pnpm install
   pnpm start
   ```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Learn more

- [ThunderID Docs](https://thunderid.dev/docs)
- [`@thunderid/node` SDK reference](https://thunderid.dev/docs/sdks/javascript/node)
