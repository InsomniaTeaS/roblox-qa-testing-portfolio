# Roblox QA Testing Portfolio

This is a QA case study based on a Roblox disaster-survival game I have been building and testing.

I made this repository because a map can look fine in Studio and still fail when a player tries to climb a ladder, cross a bridge, survive two hazards at once, or read a warning on a smaller screen. My goal was to turn those problems into reports another developer could reproduce without guessing.

## What I tested

- Player movement and map navigation
- Disaster interactions and state resets
- Object placement, clipping, and collision
- Warning cards and smaller-screen layouts

## What is included

- `docs/test-plan.md`
- `docs/bug-reports.md`
- `docs/regression-checklist.md`
- `data/bug-log.csv`
- `data/test-cases.csv`

## How I handled the work

I tested from the player's point of view, repeated each problem, and separated the expected result from what actually happened. I ranked severity by how much the issue affected normal play.

I use these severity levels:

- **Critical:** major system failure or broken round state
- **High:** blocks movement or an important feature
- **Medium:** noticeable issue with a workaround
- **Low:** mostly visual or minor usability problem

## What I learned

The main lesson was that “present” does not mean “usable.” A ladder can exist but still be blocked at the top. A bridge can look connected from above but leave a gap at foot level. Two hazards can work separately and fail when they run together.

I also learned that a useful bug report should make the next step clear. The developer should know where the issue is, how to reproduce it, and what a successful fix should look like.

## Limitations

This is a cleaned portfolio version of my testing notes. It does not include private production code or game files. I plan to add before-and-after screenshots from a stable build later.
