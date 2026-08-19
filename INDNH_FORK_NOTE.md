# InDepthNH Fork of CourtListener

This is a fork of [freelawproject/courtlistener](https://github.com/freelawproject/courtlistener) maintained by InDepthNH for accountability-journalism work.

## Why this fork exists

We do **not** modify the CourtListener codebase itself. This fork is used only for:

1. **Scheduling a daily sync** from CourtListener to the InDepthNH dashboard via GitHub Actions.
2. **Storing workflow files** under `.github/workflows/` that call the InDepthNH dashboard API.
3. **Tracking upstream changes** so we can stay aware of API changes that might affect our sync.

## Daily sync

- Workflow: `.github/workflows/courtlistener-sync.yml`
- Runs: daily at 06:00 UTC
- Endpoint: `https://dashboard.aaronrdavis.news/api/court-listener/sync`
- The sync endpoint is authenticated with a `CRON_SECRET` stored in this repo's GitHub Secrets as `INDNH_CRON_SECRET`.

## No upstream changes

We will not submit pull requests from this fork unless we find a genuine bug or improvement to contribute back to Free Law Project.
