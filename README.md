# Iris

**Software Engineer & Maker**

I am a tenth-grade student based in India with a focus on firmware, web development, and game design.

## Projects

| Project | Stack | Status | Description |
|---|---|---|---|
| **Ergographia** | TypeScript, React, Electron | Active | Factory automation game emphasizing node-based logic. |
| **Stasis CNC Router** | C++, Arduino, GRBL | In Progress | 3-axis CNC router built for Hack Club Stasis (May 2026). |
| **Stasis Combat Robot** | C++, ESP32 | In Progress | WiFi/BLE controlled combat robot. |
| **Stasis Laser Engraver** | C++, CoreXY | Planned | CoreXY-based laser engraver. |

## Technical Stack

**Languages**
TypeScript, Rust, Go, C++, Python, Java, C#, JavaScript

**Frameworks & Tools**
React, Electron, Node.js, .NET, Arduino, Docker, Linux, Firebase

## GitHub Metrics

<div align="center">

<img src="github/metrics.base.svg" alt="Base Metrics" width="49%" />
<img src="github/metrics.activity.svg" alt="Activity" width="49%" />

<img src="github/metrics.languages.svg" alt="Languages" width="49%" />
<img src="github/metrics.habits.svg" alt="Habits" width="49%" />

<img src="github/metrics.achievements.svg" alt="Achievements" width="49%" />
<img src="github/metrics.stars.svg" alt="Stars" width="49%" />

<img src="github/metrics.recent.svg" alt="Recent Activity" width="100%" />

</div>

## Contact

- **GitHub:** [irislgtm](https://github.com/irislgtm)
- **Instagram:** [@iristhep1anist](https://instagram.com/iristhep1anist)

---

<details>
<summary>GitHub Actions Metrics Configuration</summary>

<br>

Create .github/workflows/metrics.yml in your profile repository with the following configuration. Each job generates one of the SVG files referenced above.

You will need a METRICS_TOKEN secret in your repo for data gathering. Give it ead:user and ead:org; add epo only if you want private activity or private repositories included. The workflow below uses the built-in GITHUB_TOKEN to write the generated SVGs back to the repo.

`yaml
name: Metrics

on:
  schedule:
    - cron: "0 */12 * * *"   # runs every 12 hours
  workflow_dispatch:           # manual trigger
  push:
    branches: [main]

permissions:
  contents: write

jobs:

  base-stats:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          committer_token: ${{ github.token }}
          filename: github/metrics.base.svg
          base: header, repositories, metadata
          plugin_lines: yes
          plugin_traffic: yes

  activity:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          committer_token: ${{ github.token }}
          filename: github/metrics.activity.svg
          base: ""
          plugin_activity: yes
          plugin_activity_limit: 10
          plugin_activity_days: 14
          plugin_activity_visibility: public
          plugin_activity_filter: issue, pr, release, fork, review, ref/create

  languages:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          committer_token: ${{ github.token }}
          filename: github/metrics.languages.svg
          base: ""
          plugin_languages: yes
          plugin_languages_indepth: yes
          plugin_languages_details: lines, bytes-size, percentage
          plugin_languages_limit: 10
          plugin_languages_analysis_timeout: 30

  habits:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          committer_token: ${{ github.token }}
          filename: github/metrics.habits.svg
          base: ""
          plugin_habits: yes
          plugin_habits_from: 200
          plugin_habits_days: 14
          plugin_habits_facts: yes
          plugin_habits_charts: yes

  achievements:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          committer_token: ${{ github.token }}
          filename: github/metrics.achievements.svg
          base: ""
          plugin_achievements: yes
          plugin_achievements_threshold: C
          plugin_achievements_display: detailed

  stars:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          committer_token: ${{ github.token }}
          filename: github/metrics.stars.svg
          base: ""
          plugin_stargazers: yes
          plugin_stargazers_charts_type: chartjs

  recent:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          committer_token: ${{ github.token }}
          filename: github/metrics.recent.svg
          base: ""
          plugin_notable: yes
          plugin_notable_repositories: yes
          plugin_reactions: yes
          plugin_reactions_limit: 200
          plugin_reactions_display: relative
`

After committing this workflow and letting it run once, all the SVG files will appear in github/ at the root of your profile repo and the cards will render live in this README.

</details>
