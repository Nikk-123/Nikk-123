<div align="center">
 
<h1 align="center">Hi there, I'm Chayan <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px"></h1>

 <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Inter&weight=600&size=25&pause=1000&color=F75C7E&center=true&vCenter=true&width=500&lines=Software+Developer;Machine+Learning+Enthusiast;" alt="Typing SVG" /></a>

 <p>
    <em>Computer Science Student • ML Practitioner • Full Stack Developer</em>
 </p>

 <a href="https://chayan.live"><img src="https://img.shields.io/badge/View_Portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white" /></a>
 <a href="https://www.linkedin.com/in/chayan-das-a863aa25a/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>

 <br/>
</div>

---

### ⚡ Overview

I am a CSE student bridging the gap between data science and application development. My current focus is integrating **Computer Vision models** into real-time **Flask** applications.

- 🔭 I’m currently working on **Dockerizing ML pipelines**.
- 🌱 I’m currently learning **Advanced PyTorch & Cloud Deployment**.
- 💬 Ask me about **Python, Computer Vision, and Backend Logic**.

---

### 🛠️ Languages and Tools

<div align="center">
  <img src="https://skillicons.dev/icons?i=python,cpp,c,js,dart,php" /> 
  <img src="https://skillicons.dev/icons?i=flask,nodejs,flutter,html,css" /> <br>
  <img src="https://skillicons.dev/icons?i=tensorflow,pytorch,opencv,mongodb,mysql" /> 
  <img src="https://skillicons.dev/icons?i=docker,aws,gcp,azure,git,jira,postman,vscode" />
</div>

---



### Featured Project

<div align="center">
  <p><strong>Space Shooter</strong> - open-source space shooter game.</p>
  <a href="https://github.com/czl9707/gh-space-shooter">
    <img src="https://img.shields.io/badge/Space_Shooter-View_Repo-000?style=for-the-badge&logo=github&logoColor=white" />
  </a>
</div>

---

### Space Shooter Usage

**One-time Generation**

A web interface is available for on-demand GIF generation without installing anything locally.

**GitHub Action**

Automatically update your game GIF daily using GitHub Actions. Add this workflow to your repository at `.github/workflows/update-game.yml`:

```yaml
name: Update Space Shooter Game

on:
  schedule:
    - cron: '0 0 * * *'  # Daily at midnight UTC
  workflow_dispatch:  # Allow manual trigger

permissions:
  contents: write

jobs:
  update-game:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: czl9707/gh-space-shooter@v1
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
          output-path: 'game.gif'
          strategy: 'random'
```

Then display it in your README:

![My GitHub Game](game.gif)

**Action Inputs**

- `github-token` (required): GitHub token for fetching contributions
- `username` (optional): Username to generate game for (defaults to repo owner)
- `output-path` (optional): Where to save the GIF (default: `gh-space-shooter.gif`)
- `strategy` (optional): Attack pattern - column, row, or random (default: random)
- `fps` (optional): Frames per second for the animation (default: `40`)
- `commit-message` (optional): Commit message for the update

**From PyPI**

```bash
pip install gh-space-shooter
```

**From Source**

```bash
# Clone the repository
git clone https://github.com/yourusername/gh-space-shooter.git
cd gh-space-shooter

# Install with uv
uv sync

# Or with pip
pip install -e .
```

**Setup**

Create a GitHub Personal Access Token:

1. Go to https://github.com/settings/tokens
2. Click "Generate new token (classic)"
3. Select scopes: `read:user`
4. Copy the generated token

Set up your environment:

```bash
# Copy the example env file
touch .env
echo "GH_TOKEN=your_token_here" >> .env
```

Alternatively, export the token directly:

```bash
export GH_TOKEN=your_token_here
```

**Usage**

Generate your game GIF:

```bash
# Basic usage - generates username-gh-space-shooter.gif
gh-space-shooter <username>

# Examples
gh-space-shooter torvalds
gh-space-shooter octocat

# Specify custom output filename
gh-space-shooter torvalds --output my-epic-game.gif
gh-space-shooter torvalds -o my-game.gif

# Choose enemy attack strategy
gh-space-shooter torvalds --strategy row      # Enemies attack in rows
gh-space-shooter torvalds -s random           # Random chaos (default)

# Adjust animation frame rate
gh-space-shooter torvalds --fps 25            # Lower frame rate, smaller file size
gh-space-shooter torvalds --fps 40            # Default frame rate, larger file size

# Stop the animation earlier
gh-space-shooter torvalds --max-frame 200     # Stop after 200 frames
```

This creates an animated GIF showing:

- Your contribution graph as enemies (more contributions = stronger enemies)
- A Galaga-style spaceship battling through your coding history
- Enemy attack patterns based on your chosen strategy
- Smooth animations with randomized particle effects
- Your contribution stats displayed in the console

**Advanced Options**

```bash
# Save raw contribution data to JSON
gh-space-shooter torvalds --raw-output data.json

# Load from previously saved JSON (saves API rate limits)
gh-space-shooter --raw-input data.json --output game.gif

# Combine options
gh-space-shooter torvalds -o game.gif -ro data.json -s column
```

**Data Format**

When saved to JSON, the data includes:

```json
{
  "username": "torvalds",
  "total_contributions": 1234,
  "weeks": [
    {
      "days": [
        {
          "date": "2024-01-01",
          "count": 5,
          "level": 2
        }
      ]
    }
  ]
}
```

**License**

MIT

---

<br>

> **"Keep shipping. Keep learning. Stay consistent."**
