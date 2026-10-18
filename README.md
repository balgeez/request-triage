# Request Triage

A small, single-file tool that ranks a backlog of internal-tool requests so the highest-impact, easiest-to-fix items get built first.

**Live demo:** https://balgeez.github.io/request-triage/ (after you enable GitHub Pages, see below)

## What it does

Each request is rated 1 to 5 on how manual, stale and error-prone it is today, how many teams it touches, and how hard it is to build. The tool turns that into a priority score, ranks the backlog, and splits it into a Now / Next / Later roadmap. Items that are small to build are tagged "build directly"; bigger ones are tagged "write a spec" for an engineering partner.

The scoring is intentionally simple so a non-technical stakeholder can follow it:

- pain = weighted sum of manual, stale and error-prone ratings
- impact = pain x number of teams affected
- priority = impact / effort, scaled to 100

You can change the weights, edit any rating, and add your own requests.

## Sample data

Every request in the demo is invented for illustration. None of it comes from a real company.

## Run it

No build step and no dependencies. Open `index.html` in a browser.

## Host it on GitHub Pages

1. Create a repo named `request-triage` and add `index.html` and this README.
2. In the repo, go to Settings > Pages, choose "Deploy from a branch", pick `main` and `/ (root)`, and save.
3. Your page will be live at `https://balgeez.github.io/request-triage/` within a minute or two.

## Why I built it

I wanted to show, not just describe, how I'd start on the intake and prioritization side of an internal tools role.
