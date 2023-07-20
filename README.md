### The best way to predict the future is create it 👩‍💻 


🌌 I'm currently learning about smart contracts and tokens, also planning develop generative art
🌐 I’m looking to collaborate on Web 3.0 space with companies and people eager to tap into the potential of decentralized networks for greater individual control and privacy
⛩️ Fun fact: I love asian culture especially animes, origami and sudoku

-->
<div>
   <a href="http://www.github.com/cyber-konan">
    <img height="180em"  src="https://github-readme-streak-stats.herokuapp.com/?user=cyber-konan&theme=tokyonight&hide_border=true&layout=compact">
  </a>  
</div>

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
  
