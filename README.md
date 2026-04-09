<div align="center">

# Iris

**Software Engineer & Maker**

I am a developer based in India with a focus on firmware, web development, and game design.

<br />

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Inter&weight=500&size=16&pause=1000&color=333333&center=true&vCenter=true&width=500&lines=Firmware+Engineering;Web+Development;Game+Design)](https://git.io/typing-svg)

</div>

<br />

## Projects

| Project | Stack | Status | Description |
|:---|:---|:---:|:---|
| **Ergographia** | TypeScript, React, Electron | Active | Factory automation game emphasizing node-based logic. |
| **Stasis CNC Router** | C++, Arduino, GRBL | In Progress | 3-axis CNC router built for Hack Club Stasis (May 2026). |
| **Stasis Combat Robot** | C++, ESP32 | In Progress | WiFi/BLE controlled combat robot. |
| **Stasis Laser Engraver** | C++, CoreXY | Planned | CoreXY-based laser engraver. |

<br />

## Technical Stack

### Languages
<p>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="C++" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" alt="C#" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
</p>

### Frameworks & Tools
<p>
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Electron-191970?style=for-the-badge&logo=Electron&logoColor=white" alt="Electron" />
  <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET" />
  <img src="https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=Arduino&logoColor=white" alt="Arduino" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
</p>

<br />

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

<br />

## Contact

<p>
  <a href="https://github.com/irislgtm">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
  <a href="https://instagram.com/iristhep1anist">
    <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram" />
  </a>
</p>

---

<details>
<summary><b>GitHub Actions Metrics Configuration</b></summary>

<br>

Create .github/workflows/metrics.yml in your profile repository with the following configuration. Each job generates one of the SVG files referenced above.

You will need a METRICS_TOKEN secret in your repo for data gathering. Give it 
ead:user and 
ead:org; add 
epo only if you want private activity or private repositories included. The workflow below uses the built-in GITHUB_TOKEN to write the generated SVGs back to the repo.

\\\yaml
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
\\\

After committing this workflow and letting it run once, all the SVG files will appear in github/ at the root of your profile repo and the cards will render live in this README.

</details>
