# SetReady plugin

SetReady is a public roster of land-home and manufactured-home professionals in Florida, Georgia, Alabama, South Carolina, North Carolina, Tennessee, and Mississippi. This plugin adds the SetReady connector and a skill that plans a manufactured home on land, step by step, with a local pro for each step.

## What it contains

- **SetReady connector** (`.mcp.json`): the remote MCP server at https://setready.us/mcp with three read-only tools: `search_pros`, `assemble_crew`, and `get_profile`. You sign in with a free SetReady account the first time it is used. No API key is needed.
- **plan-land-home-build** skill: asks for the county and a few facts (land, water and sewer, the home, financing), lays out the usual order of work from survey and soil test through installation and skirting, and fills each step with the top-ranked SetReady listing in that county.

## What it sends and where

The skill runs no code and fetches nothing on its own. It asks Claude to call the SetReady tools, which send the county, state, and requested trades to https://setready.us/mcp and read back published directory listings. Each tool call counts against the account's daily allowance of 100 calls. The SetReady privacy policy is at https://setready.us/privacy and the terms are at https://setready.us/terms

## Caveats

A listing is a directory entry, not an endorsement or a booking. A license number on a listing is not a current verification; check it with the state licensing board. Coverage varies by county.

## Try it locally

```sh
git clone https://github.com/s10mcow/setready-plugin
claude --plugin-dir ./setready-plugin
```

Then run `/mcp` to sign in to SetReady, and ask: "I'm putting a doublewide on 5 acres I own in Marion County, Florida. What do I need, in order, and who can do it?"
