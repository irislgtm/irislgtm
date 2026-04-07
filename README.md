<div align="center">

```
██╗██████╗ ██╗███████╗
██║██╔══██╗██║██╔════╝
██║██████╔╝██║███████╗
██║██╔══██╗██║╚════██║
██║██║  ██║██║███████║
╚═╝╚═╝  ╚═╝╚═╝╚══════╝
```

### `they / them` &nbsp;·&nbsp; `web dev` &nbsp;·&nbsp; `firmware` &nbsp;·&nbsp; `game dev`

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=14&duration=3500&pause=800&color=3DDC84&center=true&vCenter=true&width=500&lines=building+Ergographia+%E2%80%94+a+factory+automation+game;web+%2B+firmware+%2B+hardware+hackathons;the+factory+is+the+diagram.)](https://git.io/typing-svg)

</div>

---

## `~/whoami`

> Tenth-grade student from India building things that shouldn't exist yet.
> Firmware meets front-end. Node graphs meet factory lines. Started with ZenScript, never stopped.

Currently working on **[Ergographia](https://github.com/irislgtm/ergographia)** — a Windows 95-themed factory automation game where the diagram *is* the factory.
Also preparing three builds for **Hack Club Stasis** (May 2026): a combat robot, a CNC router, and a CoreXY laser engraver.

---

## `~/stack`

<div align="center">

**Languages**

![TypeScript](https://img.shields.io/badge/TypeScript-1a1a2e?style=flat-square&logo=typescript&logoColor=3DDC84)
![Rust](https://img.shields.io/badge/Rust-1a1a2e?style=flat-square&logo=rust&logoColor=3DDC84)
![Go](https://img.shields.io/badge/Go-1a1a2e?style=flat-square&logo=go&logoColor=3DDC84)
![C++](https://img.shields.io/badge/C++-1a1a2e?style=flat-square&logo=cplusplus&logoColor=3DDC84)
![Python](https://img.shields.io/badge/Python-1a1a2e?style=flat-square&logo=python&logoColor=3DDC84)
![Java](https://img.shields.io/badge/Java-1a1a2e?style=flat-square&logo=openjdk&logoColor=3DDC84)
![C#](https://img.shields.io/badge/C%23-1a1a2e?style=flat-square&logo=csharp&logoColor=3DDC84)
![JavaScript](https://img.shields.io/badge/JavaScript-1a1a2e?style=flat-square&logo=javascript&logoColor=3DDC84)

**Frameworks & Tools**

![React](https://img.shields.io/badge/React-1a1a2e?style=flat-square&logo=react&logoColor=3DDC84)
![Electron](https://img.shields.io/badge/Electron-1a1a2e?style=flat-square&logo=electron&logoColor=3DDC84)
![Node.js](https://img.shields.io/badge/Node.js-1a1a2e?style=flat-square&logo=nodedotjs&logoColor=3DDC84)
![Arduino](https://img.shields.io/badge/Arduino-1a1a2e?style=flat-square&logo=arduino&logoColor=3DDC84)
![Docker](https://img.shields.io/badge/Docker-1a1a2e?style=flat-square&logo=docker&logoColor=3DDC84)
![Linux](https://img.shields.io/badge/Linux-1a1a2e?style=flat-square&logo=linux&logoColor=3DDC84)
![Firebase](https://img.shields.io/badge/Firebase-1a1a2e?style=flat-square&logo=firebase&logoColor=3DDC84)
![.NET](https://img.shields.io/badge/.NET-1a1a2e?style=flat-square&logo=dotnet&logoColor=3DDC84)

</div>

---

## `~/metrics`

<!-- ═══════════════════════════════════════════════
     METRICS SETUP — GitHub Actions workflow needed
     File: .github/workflows/metrics.yml
     See setup instructions at the bottom of this README
     ═══════════════════════════════════════════════ -->

<div align="center">

### Activity & Stats

<!-- METRICS: Base stats + activity calendar -->
<img src="github/metrics.base.svg" alt="Base Metrics" width="49%" />
<img src="github/metrics.activity.svg" alt="Activity" width="49%" />

### Languages & Habits

<!-- METRICS: Top languages (indepth) + coding habits -->
<img src="github/metrics.languages.svg" alt="Languages" width="49%" />
<img src="github/metrics.habits.svg" alt="Habits" width="49%" />

### Achievements & Stargazers

<!-- METRICS: Achievements + star history -->
<img src="github/metrics.achievements.svg" alt="Achievements" width="49%" />
<img src="github/metrics.stars.svg" alt="Stars" width="49%" />

### Recently Active

<!-- METRICS: Recent activity feed -->
<img src="github/metrics.recent.svg" alt="Recent Activity" width="100%" />

</div>

---

## `~/projects`

| Project | Stack | Status | Description |
|---|---|---|---|
| **Ergographia** | TypeScript · React · Electron | `active` | Windows 95-themed factory automation game. Node-graph core. |
| **Stasis CNC Router** | C++ · Arduino / GRBL | `in progress` | 3-axis CNC for Hack Club Stasis (May 2026) |
| **Stasis Combat Robot** | C++ · ESP32 | `in progress` | WiFi/BLE combat robot, same hackathon |
| **Stasis Laser Engraver** | C++ · CoreXY | `planned` | CoreXY laser engraver build |
| **Builder's Wand** | Java · Forge 1.12.2 | `spec complete` | Minecraft mod consolidating Extra Utilities 2, Building Gadgets, Effortless Building |

---

## `~/connect`

<div align="center">

[![Instagram](https://img.shields.io/badge/@iristhep1anist-1a1a2e?style=flat-square&logo=instagram&logoColor=3DDC84)](https://instagram.com/iristhep1anist)
[![GitHub](https://img.shields.io/badge/irislgtm-1a1a2e?style=flat-square&logo=github&logoColor=3DDC84)](https://github.com/irislgtm)

</div>

---

<details>
<summary><code>~/metrics/setup</code> — how to generate these cards</summary>

<br>

Create `.github/workflows/metrics.yml` in your profile repository with the following configuration. Each job generates one of the SVG files referenced above.

You will need a `METRICS_TOKEN` secret in your repo — a GitHub personal access token with `read:user`, `repo`, and `read:org` scopes.

```yaml
name: Metrics

on:
  schedule:
    - cron: "0 */12 * * *"   # runs every 12 hours
  workflow_dispatch:           # manual trigger
  push:
    branches: [main]

jobs:

  base-stats:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
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
          filename: github/metrics.activity.svg
          base: ""
          plugin_activity: yes
          plugin_activity_limit: 10
          plugin_activity_days: 14
          plugin_activity_filter: all

  languages:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
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
          filename: github/metrics.recent.svg
          base: ""
          plugin_notable: yes
          plugin_notable_repositories: yes
          plugin_reactions: yes
          plugin_reactions_limit: 200
          plugin_reactions_display: relative
```

After committing this workflow and letting it run once, all the SVG files will appear in `github/` at the root of your profile repo and the cards will render live in this README.

</details>

---

<div align="center">
<sub>built with too much coffee and not enough sleep · india · 2026</sub>
</div>