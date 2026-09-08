<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d0d1a,50:4c1d95,100:7c3aed&height=210&section=header&text=SRIDHAR%20S&fontSize=50&fontColor=ffffff&fontAlignY=35&animation=fadeIn&desc=Full-Stack%20AI%20Engineer%20%7C%20Cinematic%20Web%20%2B%20Applied%20ML&descAlignY=58&descSize=16&descColor=c4b5fd"/>

<br/>

<a href="https://www.linkedin.com/in/sridhar-s-242004"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:sridhar242004@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://github.com/sridhar242004?tab=repositories"><img src="https://img.shields.io/badge/113_Repositories-181717?style=for-the-badge&logo=github&logoColor=white"/></a>
<a href="https://quantumviz-vercel.vercel.app/"><img src="https://img.shields.io/badge/QuantumViz_AI-Live_Demo-06b6d4?style=for-the-badge&logo=vercel&logoColor=white"/></a>

</div>

<br/>

I'm a Full-Stack AI Engineer out of Tamil Nadu, India — a B.E. in Computer Science from Hindustan Institute of Technology and Science (2025), an IEEE-published author on ML-based travel recommendation systems, an AWS Certified Cloud Practitioner, and an IET member. This account carries 113 public repositories built since 2023, split across two genuinely different kinds of engineering.

**Most of what's below ships as a single HTML file with no backend at all** — Three.js and GSAP for the motion, the Groq LPU (`llama-3.3-70b-versatile`) wired in wherever a project needs intelligence, deployed to Vercel or Netlify the same day it's written. **A smaller set is real ML infrastructure** — PyTorch, CUDA, diffusion pipelines, Docker — built to actually run inference rather than demo it. Every project below is tagged so you know which lane you're looking at before you open it.

---

## Selected Work

*The five repositories pinned on this profile.*

### NeuroDraw &nbsp;·&nbsp; <sub>applied ML</sub>

A sketch-to-image pipeline that runs entirely on local hardware: ControlNet locks the output to your sketch's structure, Stable Diffusion v1.5 renders it, CLIP handles semantic alignment. The Flask backend is written like production software rather than a demo — a thread-safe singleton model manager loads weights on a background thread so the UI is usable before inference finishes loading, a single inference lock serializes GPU access instead of letting concurrent requests corrupt each other's tensors, and every failure path (OOM, bad payload, missing content-type) resolves to a typed JSON error instead of a stack trace. xFormers, VAE slicing/tiling, and `torch.compile` bring a 512×512 render down to 3–8 seconds on a single consumer GPU.

`Python` `PyTorch` `CUDA` `ControlNet` `Stable Diffusion v1.5` `CLIP` `Flask` `Docker`

[Source](https://github.com/sridhar242004/AIdrawtoimage.AI)

### MotionMaster Pro &nbsp;·&nbsp; <sub>applied ML</sub>

A dual-pipeline AI video system: I2VGenXL animates a single image, and a separate SDXL pipeline turns a scene-by-scene storyboard into a fully-scored short film — gTTS narration and mood-matched music mixed with Pydub, assembled with MoviePy, encoded through ffmpeg. Built to survive a 24GB Colab GPU without falling over: FP16 throughout, CPU offload on the video model, attention slicing on SDXL, a CUDA cache clear after every single inference. The Vercel front-end is the showcase; the pipeline itself lives in the notebook it was built for.

`Python` `PyTorch` `Diffusers` `I2VGenXL` `SDXL` `Gradio` `MoviePy` `OpenCV`

[Source](https://github.com/sridhar242004/MotionMaster) · [Live](https://motionmastor.vercel.app/)

### Neural Conjecture Proposer &nbsp;·&nbsp; <sub>cinematic build</sub>

Points a large language model at pure mathematics instead of a chat window. Choose a domain — Number Theory through Set Theory — a conjecture type, and a difficulty up to "Millennium-level," and it returns a formal LaTeX statement, motivation, related results, and proof strategies, parsed from a strict seven-section contract the system prompt enforces rather than free-form text. Six Groq-hosted models are swappable at runtime, everything renders through MathJax, and the API key never reaches the browser — the frontend only talks to a thin backend proxy.

`JavaScript` `MathJax` `GSAP` `Chart.js` `Groq API`

[Source](https://github.com/sridhar242004/MATAI)

### QuestionGenius Elite &nbsp;·&nbsp; <sub>cinematic build</sub>

Feeds a document through the Groq LPU and gets back structured, pedagogically-calibrated exam questions in under two seconds — no React, no build step, two HTML files and a thin Node proxy. Every visual effect on the page — scramble-text hero, magnetic cursor, 3D-tilt cards — is hand-written CSS and JS, and it still clears a Lighthouse score of 94+. If the backend is unreachable, a regex-based offline generator keeps the tool working.

`Vanilla JS` `CSS` `Node.js` `Groq API`

[Source](https://github.com/sridhar242004/question-qenius) · [Live](https://questiongenius-vercel-fixed.vercel.app/)

### QuantumViz AI &nbsp;·&nbsp; <sub>cinematic build</sub>

A data platform with no backend at all: drop in a CSV, run it through one of 15 client-side ML algorithms, pick from 12 chart types across Chart.js, D3, and Plotly — while Groq streams a plain-language read of what the chart shows as it renders. Every analysis step happens in the browser; nothing round-trips to a server.

`React` `D3.js` `Plotly.js` `Chart.js` `Groq API`

[Source](https://github.com/sridhar242004/Quantum_Interactivecharts) · [Live](https://quantumviz-vercel.vercel.app/)

---

## Fundamentals Lab

Before the branded builds, the basics — kept public as a record of the climb rather than polished for show. [trees_DSA](https://github.com/sridhar242004/trees_DSA) and [graphs_DSA](https://github.com/sridhar242004/graphs_DSA) visualize graph and tree algorithms; [linked_DSA](https://github.com/sridhar242004/linked_DSA) and [Sort_Master](https://github.com/sridhar242004/Sort_Master) cover linked lists and sorting. [Virtual_keyboard](https://github.com/sridhar242004/Virtual_keyboard) — an OpenCV + MediaPipe air-typing keyboard that tracks hand landmarks in real time — is the highest-starred repo on the account, built as a single file. A handful of browser games ([snake-game](https://github.com/sridhar242004/snake-game), [flappy-bird](https://github.com/sridhar242004/flappy-bird), [shooter-game](https://github.com/sridhar242004/shooter-game)) and the earliest clone practice ([Netflix-clone](https://github.com/sridhar242004/Netflix-clone), [youtube-clone](https://github.com/sridhar242004/youtube-clone), a Java banking system from the certified internship) round out the rest.

---

<details>
<summary><strong>More from the catalog</strong> — 12 of the other 100+ repos</summary>
<br/>

| Project | What it does |
|---|---|
| [IdeaSpark](https://github.com/sridhar242004/idea_generator) | Groq-streamed business/idea generator with a neural-network hero |
| [LinguaFlow](https://github.com/sridhar242004/translator_AI) | Real-time context-aware translation with a 3D language globe |
| [HealthTwin](https://github.com/sridhar242004/Health-Twin) | Predictive-health dashboard, DNA-helix hero, Groq health chat |
| [GeneX](https://github.com/sridhar242004/Interactive-Genomic-Data-Explorer) | D3-driven genome browser and analyzer |
| [NEOBRUT VR Gallery](https://github.com/sridhar242004/virtual-art-gallery-and-vr-gallery) | Spline + Three.js immersive art gallery with an AI curator |
| [ARGOS](https://github.com/sridhar242004/virtual-debate) | AI debate judge and coach with post-round analytics |
| [ClimaCore Observatory](https://github.com/sridhar242004/CLIMATE-CHANGE-SIMULATOR) | Three.js Earth driven by a six-parameter climate physics engine |
| [Quantum Realm Explorer](https://github.com/sridhar242004/Quantum-Computing) | Quantum algorithm simulator with a circuit builder |
| [ResumeAI Pro](https://github.com/sridhar242004/resume-builder) | ATS-aware resume builder with a skills radar chart |
| [NEET Aspirants Hub](https://github.com/sridhar242004/NEET-Aspirants-Hub) | AI study mentor for India's NEET-UG exam, Three.js molecular hero |
| [NewsNexus](https://github.com/sridhar242004/News-Nexus) | Curated news meeting AI summarization |
| [PixelForge](https://github.com/sridhar242004/Advanced-collage-maker) | AI-assisted photo collage studio with one-click export |

The rest live in the [repositories tab](https://github.com/sridhar242004?tab=repositories).

</details>

---

## Tech Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=js,ts,python,java,html,css&theme=dark"/>
<br/><br/>
<img src="https://skillicons.dev/icons?i=react,nodejs,flask,threejs,tailwind,bootstrap&theme=dark"/>
<br/><br/>
<img src="https://skillicons.dev/icons?i=aws,docker,git,github,linux,vscode&theme=dark"/>
<br/><br/>
<img src="https://img.shields.io/badge/Groq_LPU-FF6B35?style=flat-square"/>
<img src="https://img.shields.io/badge/Anthropic_Claude-CC785C?style=flat-square&logo=anthropic&logoColor=white"/>
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/>
<img src="https://img.shields.io/badge/Stable_Diffusion-8A2BE2?style=flat-square"/>
<img src="https://img.shields.io/badge/ControlNet-7c3aed?style=flat-square"/>
<img src="https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white"/>

</div>

---

## Credentials

| | |
|---|---|
| **IEEE** | Published author — ML-based travel recommendation systems |
| **AWS** | Certified Cloud Practitioner |
| **IET** | Member |
| **National Project Exposition** | Award winner |
| **B.E. Computer Science** | Hindustan Institute of Technology and Science, 2025 |
| **Internships** | Java development · Cybersecurity |

---

## GitHub Activity

<div align="center">

<img height="165em" src="https://github-readme-stats.vercel.app/api?username=sridhar242004&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true&bg_color=0d1117&title_color=7c3aed&icon_color=06b6d4&text_color=c4b5fd&ring_color=7c3aed&border_radius=12"/>
<img height="165em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=sridhar242004&layout=donut&langs_count=8&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=7c3aed&text_color=c4b5fd&border_radius=12"/>

<br/>

<img src="https://streak-stats.demolab.com?user=sridhar242004&theme=tokyonight&hide_border=true&background=0d1117&ring=7C3AED&fire=06B6D4&currStreakLabel=c4b5fd&sideLabels=c4b5fd&currStreakNum=ffffff&sideNums=ffffff&dates=6b7280&stroke=1a0a3e&border_radius=12"/>

<br/><br/>

<img src="https://raw.githubusercontent.com/sridhar242004/sridhar242004/main/profile-3d-contrib/profile-night-rainbow.svg" alt="3D Contribution Calendar" width="100%"/>

<br/>

<img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=sridhar242004&theme=tokyo-night&bg_color=0d1117&color=7c3aed&line=06b6d4&point=7c3aed&area=true&hide_border=true&area_color=1a0a3e"/>

<br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sridhar242004/sridhar242004/output/github-contribution-grid-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/sridhar242004/sridhar242004/output/github-contribution-grid-snake.svg"/>
  <img alt="GitHub contribution snake" src="https://raw.githubusercontent.com/sridhar242004/sridhar242004/output/github-contribution-grid-snake-dark.svg"/>
</picture>

</div>

---

<div align="center">

<a href="https://www.linkedin.com/in/sridhar-s-242004"><img src="https://img.shields.io/badge/Let's_talk-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:sridhar242004@gmail.com"><img src="https://img.shields.io/badge/or_email-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>

<br/><br/>

<sub><code>sridhar@github:~$ shipping since 2023_</code></sub>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:7c3aed,50:4c1d95,100:0d0d1a&height=120&section=footer"/>

</div>

<br/>

<details>
<summary><strong>⚙️ GitHub Actions behind the widgets above</strong> — copy each into <code>.github/workflows/</code>, skip any already set up</summary>

### `.github/workflows/snake.yml` — Contribution Snake

```yaml
name: Generate Snake Animation

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches:
      - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 10

    steps:
      - name: Generate GitHub Contribution Snake
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push snake animation to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### `.github/workflows/3d-contrib.yml` — 3D Contribution Calendar

```yaml
name: Generate 3D Contribution Calendar

on:
  schedule:
    - cron: "0 18 * * *"
  workflow_dispatch:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    name: Generate 3D Contribution Graph

    steps:
      - uses: actions/checkout@v3

      - name: Generate 3D Contribution Image
        uses: yoshi389111/github-profile-3d-contrib@0.7.1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          USERNAME: sridhar242004
        with:
          MAX_REPOS: 50
          SETTING_JSON: |
            {
              "githubUserName": "sridhar242004",
              "startWeekDay": 0,
              "topLangType": "pie",
              "topLangForegroundColor": "#c4b5fd",
              "topLangBackgroundColor": "#0d1117",
              "backgroundColor": "#0d1117",
              "backgroundImage": "",
              "foregroundColor": "#7c3aed",
              "contribution": {
                "topColorCommit": "#7c3aed",
                "secondColorCommit": "#06b6d4",
                "thirdColorCommit": "#10b981",
                "fourthColorCommit": "#f59e0b",
                "rainyDayColor": "#1e1b4b",
                "textForegroundColor": "#c4b5fd",
                "textBackgroundColor": "transparent"
              }
            }

      - name: Commit & Push 3D Calendar
        uses: EndBug/add-and-commit@v7.5.0
        with:
          message: "chore: regenerate 3D contribution calendar [skip ci]"
          add: "profile-3d-contrib/"
```

### `.github/workflows/metrics.yml` — Advanced Analytics Card (optional, needs a `METRICS_TOKEN` secret)

```yaml
name: Generate GitHub Metrics

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write

    steps:
      - name: Generate Metrics
        uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          user: sridhar242004
          template: classic
          base: header, activity, community, repositories
          config_timezone: Asia/Kolkata
          plugin_languages: yes
          plugin_languages_indepth: yes
          plugin_languages_details: bytes-size, lines, percentage
          plugin_languages_limit: 8
          plugin_topics: yes
          plugin_topics_limit: 15
          plugin_stars: yes
          plugin_stars_limit: 4
          plugin_achievements: yes
          plugin_achievements_display: compact
          plugin_achievements_secrets: yes
          plugin_achievements_limit: 0
          config_order: base.header, base.activity, languages, topics, stars, achievements
          filename: github-metrics.svg
          output_action: commit
          committer_branch: github-metrics
          committer_message: "chore: update GitHub metrics [skip ci]"
```

</details>
