# listing-alert-agent – your private state

This repository holds **your** settings and history for the [listing-alert-agent](https://github.com/murugkarpratik44/listing-alert-agent) Claude plugin.

## Create your copy

1. Select **Use this template → Create a new repository** on GitHub.
2. Set visibility to **Private**. Your copy will hold your budget, the places that matter to you and the listings you were sent.
3. In Claude, run the plugin's `setup` skill and give it the name of your new repository (for example `your-name/my-listing-alerts`).

Setup asks you questions and fills in the files below. You do not need to edit them by hand, but you can.

## What is in here

| Path | What it holds | Written by |
|---|---|---|
| `config/profile.yaml` | What you want, budget, search areas, alert preferences | `setup`, `tune` |
| `config/sources.yaml` | Which sites' alert emails to read, by exact sender address | `setup` |
| `config/places.yaml` | Places that matter to you, and the places listings may come from | `setup` |
| `data/travel-cache.csv` | Travel times from each search place to each place that matters | `setup` (refreshed monthly) |
| `data/listings.csv` | One row per listing you were alerted about (facts only) | each alert run |
| `data/run-log.csv` | One row per run: emails read, listings reported, health | each alert run |
| `data/feedback.csv` | Your verdicts on listings ("too far", "no parking") | `tune` (v0.2) |
| `data/benchmark/` | Optional copy of the market-average file | `setup` |
| `SETUP-SUMMARY.md` | Your setup in plain English | `setup` |

## Privacy

- Keep this repository private.
- No passwords or API keys belong here. A travel-time API key, if you use one, is kept as an environment variable or a sensitive plugin setting, never in a file.
- `listings.csv` stores listing facts only: never names, phone numbers or email addresses of landlords, agents or sellers.
