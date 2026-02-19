# .github (Profile + Automation)

Costa Rica

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[brown9804](https://github.com/brown9804)

Last updated: 2025-05-13

----------

> This repository holds the public **GitHub profile content** for *Microsoft Cloud Sandbox - Unofficial* and a small **GitHub Actions automation** that refreshes the visitor/view counter badge.

## What this is for

- **Profile hub**: the content in `profile/README.md` is intended to be displayed on the GitHub profile page (when this repository is the special `.github` repo for an organization).
- **Visitor counter updates**: a scheduled GitHub Actions workflow updates the badge inside the profile README and writes view history to `metrics.json`.

## Repository layout

- `profile/README.md`
  - The main profile page content (about the Microsoft Cloud hub, disclaimers, and the view counter badge).
- `.github/workflows/use-visitor-counter.yml`
  - GitHub Actions workflow that runs on a schedule / manual trigger to update the badge and regenerate `metrics.json`.
- `metrics.json`
  - Generated historical view metrics (daily counts + uniques). This file is overwritten by the workflow.

## How to update

### Update the profile text

Edit `profile/README.md`.

### Refresh the visitor counter badge / metrics

- Run the workflow manually from GitHub: **Actions** → **Use Visitor Counter Logic** → **Run workflow**.
- Or let it run automatically on the configured cron schedule.

## Secrets / permissions

The workflow expects a repository secret named `TRAFFIC_TOKEN` so it can read repository traffic insights.

## Notes

- The workflow uses an external tool repo (`brown9804/github-visitor-counter`) to generate the badge and `metrics.json`.
- Manual edits to `metrics.json` are not recommended because the workflow will replace it on the next run.

<!-- START BADGE -->
<div align="center">
  <img src="https://img.shields.io/badge/Total%20views-1280-limegreen" alt="Total views">
  <p>Refresh Date: 2026-01-06</p>
</div>
<!-- END BADGE -->
