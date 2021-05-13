# Visit https://github.com/lowlighter/metrics/blob/master/action.yml for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          token: ${{ secrets.METRICS_TOKEN }}

![Metrics](https://metrics.lecoq.io/Cliffy57?template=classic&repositories.forks=true&isocalendar=1&isocalendar.duration=full-year&config.timezone=Europe%2FParis&config.twemoji=true)

          # Options
          user: Cliffy57
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Europe/Paris
          config_twemoji: yes
          plugin_isocalendar: yes
          plugin_isocalendar_duration: full-year
          repositories_forks: yes
          
