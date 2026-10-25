<h1 align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=30&pause=1000&color=2196F3&center=true&vCenter=true&width=435&lines=Namaste!;I'm+Krishna+Maheshwari;Software+Developer;Always+Learning" alt="Typing SVG" />
</h1>

<p align="center">
  <em>Building digital solutions & cracking problems on LeetCode 🚀</em>
</p>
<br/>

### 🛠️ What I Use
<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=cpp,java,js,react,nodejs,git,linux&perline=7" alt="Skills" />
  </a>
</p>

### ⚡ Quick Facts
- 🔭 Currently building: **Apna Latest Project Yahan Likho**
- 💡 Exploring: **Nayi Skill Yahan Likho**
- 🤝 Open to collaborate on: **Open Source Projects**
- 📬 How to reach me: **Apna LinkedIn URL Yahan Dalo**

### 🐍 Contribution Graph
<p align="center">
  <!-- 'KRISHNA_USERNAME' ko apne asli GitHub handle se replace karna -->
  <img src="https://raw.githubusercontent.com/KRISHNA_USERNAME/KRISHNA_USERNAME/output/github-contribution-grid-snake.svg" alt="Snake Graph" />
</p>

name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *" # Har raat 12 baje auto-update hoga
  workflow_dispatch: # Tumhe manual run karne ka button dega

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Generate Snake Animation
        uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg

      - name: Push to Output Branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
