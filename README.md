# Request Triage

**Live demo: https://balgeez.github.io/request-triage/**

Most teams have more tool requests than people to build them. This is a small tool I made to show how I'd decide what to build first.

You give each request a 1 to 5 rating for how manual, stale and error-prone the current process is, how many teams it affects, and how hard it would be to build. The tool ranks the backlog, sorts it into Now / Next / Later, and flags each item as either something to build directly (a script, a no-code tool) or something that needs a written spec for an engineer.

## Try it

- Change any rating and watch the ranking reshuffle.
- Move the weight sliders. If you care more about error-prone reports than stale ones, the order changes.
- Add your own request at the bottom of the left panel.

## How the score works

I kept it simple on purpose, so anyone in a prioritization meeting can follow it:

- **Pain** = manual + stale + error-prone, each multiplied by its weight
- **Impact** = pain x number of teams affected
- **Priority** = impact / effort, scaled to 0 to 100

Effort of 1 or 2 means "build directly." Effort of 3 or more means "write a spec."

## What this is not

- All the sample requests are made up. None of it comes from a real company.
- It's a single HTML file. Nothing is saved when you refresh the page.
- The 1 to 5 ratings are judgment calls, not measurements. In real use I'd want to back them with data where possible (hours spent per week, number of corrections per month).

## If I built this for real

I'd connect it to an intake form so requests arrive already rated, store them somewhere shared, and let each team see where their request sits and why. I'd also check the scoring against what actually shipped and adjust the weights.

## Built with

Plain HTML, CSS and JavaScript. No frameworks, no build step. Open `index.html` in a browser to run it locally.

Made by [Baljeet Singh](https://github.com/balgeez).
