name: Generate Snake Animation

on:
  schedule:
    - cron: "0 0 * * *" # Runs every day at midnight UTC
  workflow_dispatch: # Allows you to run it manually

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3

      - name: Generate Snake
        uses: Platane/snk@v3
        with:
          github_user_name: cristalblues393-commits
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push result
        run: |
          git config --global user.name "github-actions[bot]"
          git config --global user.email "41898282+github-actions[bot]@users.noreply.github.com"
          git add dist/
          git commit -m "Update snake animation"
          git push
