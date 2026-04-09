# GitHub Repo Stats

This repository collects and stores long-term GitHub repository analytics for the public repositories of [AiratTop](https://github.com/AiratTop) using the [github-repo-stats](https://github.com/jgehrcke/github-repo-stats) GitHub Action.

## Features

- **Long-term history:** Stores repository traffic snapshots over time, beyond GitHub’s default short retention window.
- **Multi-repository tracking:** Collects analytics for multiple public repositories from a single workflow.
- **Automatic updates:** Runs daily on a scheduled GitHub Actions workflow.
- **Manual runs:** Supports manual workflow execution with `workflow_dispatch`.
- **Centralized storage:** Stores generated data and reports in a dedicated branch of this repository.
- **Simple setup:** Works with a single GitHub token stored in repository secrets.
- **Public and free-friendly:** Well suited for tracking public repositories with GitHub-hosted runners.

## Tracked Repository Groups

### Profile

- [**AiratTop**](https://github.com/AiratTop/AiratTop)

### Self-hosted

- [**authentik-self-hosted**](https://github.com/AiratTop/authentik-self-hosted)
- [**beszel-self-hosted**](https://github.com/AiratTop/beszel-self-hosted)
- [**caddy-self-hosted**](https://github.com/AiratTop/caddy-self-hosted)
- [**clickhouse-self-hosted**](https://github.com/AiratTop/clickhouse-self-hosted)
- [**gatus-self-hosted**](https://github.com/AiratTop/gatus-self-hosted)
- [**metabase-self-hosted**](https://github.com/AiratTop/metabase-self-hosted)
- [**monitoring-self-hosted**](https://github.com/AiratTop/monitoring-self-hosted)
- [**mysql-self-hosted**](https://github.com/AiratTop/mysql-self-hosted)
- [**n8n-self-hosted**](https://github.com/AiratTop/n8n-self-hosted)
- [**ollama-self-hosted**](https://github.com/AiratTop/ollama-self-hosted)
- [**postgresql-self-hosted**](https://github.com/AiratTop/postgresql-self-hosted)
- [**qdrant-self-hosted**](https://github.com/AiratTop/qdrant-self-hosted)
- [**redis-self-hosted**](https://github.com/AiratTop/redis-self-hosted)
- [**wordpress-self-hosted**](https://github.com/AiratTop/wordpress-self-hosted)

### API

- [**dns.api.airat.top**](https://github.com/AiratTop/dns.api.airat.top)
- [**ip.api.airat.top**](https://github.com/AiratTop/ip.api.airat.top)
- [**meta.api.airat.top**](https://github.com/AiratTop/meta.api.airat.top)
- [**num2words.api.airat.top**](https://github.com/AiratTop/num2words.api.airat.top)
- [**translit.api.airat.top**](https://github.com/AiratTop/translit.api.airat.top)
- [**uuid.api.airat.top**](https://github.com/AiratTop/uuid.api.airat.top)
- [**whois.api.airat.top**](https://github.com/AiratTop/whois.api.airat.top)

### Tools / Web Apps / Services

- [**ad-generator**](https://github.com/AiratTop/ad-generator)
- [**json.airat.top**](https://github.com/AiratTop/json.airat.top)
- [**md.airat.top**](https://github.com/AiratTop/md.airat.top)
- [**miner.airat.top**](https://github.com/AiratTop/miner.airat.top)
- [**mytasks**](https://github.com/AiratTop/mytasks)
- [**pass.airat.top**](https://github.com/AiratTop/pass.airat.top)
- [**random.airat.top**](https://github.com/AiratTop/random.airat.top)
- [**task.airat.top**](https://github.com/AiratTop/task.airat.top)
- [**utm.airat.top**](https://github.com/AiratTop/utm.airat.top)
- [**uuid.airat.top**](https://github.com/AiratTop/uuid.airat.top)

### Utility / Misc

- [**imagemagick-watermark**](https://github.com/AiratTop/imagemagick-watermark)
- [**phpmyadmin-update**](https://github.com/AiratTop/phpmyadmin-update)

## Workflow

This repository uses a GitHub Actions workflow located at:

```text
.github/workflows/repo-stats.yml
````

The workflow:

1. Runs daily on schedule.
2. Can be started manually from the GitHub Actions tab.
3. Iterates through the configured list of repositories.
4. Collects repository traffic and related analytics.
5. Stores the generated data in a dedicated branch.

## Data Storage

Generated analytics data is stored in a separate branch:

```text
github-repo-stats
```

This keeps the `main` branch clean while allowing the action to continuously append and update analytics artifacts over time.

## Requirements

* A public GitHub repository for storing workflow configuration and generated analytics.
* A GitHub personal access token stored in repository secrets.
* Repository secret name:

```text
GHRS_GITHUB_API_TOKEN
```

## Usage

### Run manually

1. Open the **Actions** tab in this repository.
2. Select the `repo-stats` workflow.
3. Click **Run workflow**.

### Wait for scheduled collection

The workflow also runs automatically every day based on the configured cron schedule.

## Notes

* The first useful analytics history appears only after multiple workflow runs.
* The repository accumulates snapshots over time, so the value grows gradually.
* This setup is intended for public repositories and a simple, low-maintenance analytics workflow.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Author

**AiratTop**

* Website: [airat.top](https://airat.top)
* GitHub: [@AiratTop](https://github.com/AiratTop)
* Email: [mail@airat.top](mailto:mail@airat.top)
* Repository: [github-repo-stats](https://github.com/AiratTop/github-repo-stats)
