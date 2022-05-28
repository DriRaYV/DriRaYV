## Hi there 💘, my name is Rafaella.
## I'm a student off systems development.

- 👨‍💻I'm currently learning: JAVA SCRIPT / HTML / CSS / DATABASE/ OPERATING SYSTEMS
- 💌Ask me about:  GIT BASH
- 📬How to reach me: rafaellagdh55@gmail.com
- 🚹Pronouns: SHE/HER
- ⚡ my favorite phrase: "We were born to make history" 

my projects are for trainning, so you can use with the mit liscense.

Thank you for reading!!💞


name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
