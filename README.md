# Hive Personal Archive

A small, static web app for exploring a public Hive account's post history.

## What it does

- Loads public posts from Hive's `bridge.get_account_posts` API
- Searches title/body
- Filters by year and tag
- Shows post count, years, and tags
- Links each post to PeakD
- Exports the loaded archive as JSON or Markdown
- Does not request or store Hive private keys

## Run locally

Open `index.html` in a browser, or serve the folder with any static web server.

## Netlify

This repository is intentionally dependency-free. Netlify can deploy it directly.

Build command: leave blank  
Publish directory: `.`

`netlify.toml` is included for this configuration.

## GitHub

Create a repository and upload:

- `index.html`
- `netlify.toml`
- `README.md`

Then connect the repository in Netlify: Add new project → Import an existing project → choose GitHub → select the repository → Publish.

## Notes

The app currently loads up to 2,000 authored posts per session (20 pages × 100). This is an MVP; a production archive should add durable indexing, pagination controls, caching, and a backend/HAF-based index for very large accounts.
