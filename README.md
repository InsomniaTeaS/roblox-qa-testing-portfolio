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

## Screenshots from the test pass

These are raw captures from the map review. I kept the surrounding geometry visible because it helps show why a route or placement problem matters during normal play.

docs/images/Screenshot 2026-07-24 010242.png

More examples are included in the detailed bug reports:

- Blocked and misaligned ladder routes
- A bridge or elevated route that does not connect cleanly
- Props clipping into stairs or nearby structures

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

This is a cleaned portfolio version of my testing notes. It does not include private production code or game files. The screenshots show issues from a development build, so they are evidence of the test pass rather than final promotional images. I plan to add before-and-after comparisons after the related fixes are verified.
