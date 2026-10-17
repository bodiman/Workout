# Gym Log

A tiny, single-file workout tracker with a built-in 8-week plan. Open `index.html` in any browser. No build, no server.

## The plan

Supplemental strength work around ~6 h/week of gymnastics (Mon, Tue, Thu evenings) and ~3 h/week of climbing (Wed and some Sat evenings). Three gym days (Wed, Fri, Sun), 2 sets per exercise. Bench Press, Lat Pulldown and Zanetti Press are hit twice a week.

| Wed: Upper (heavy, morning; climb that evening) | Fri: Legs | Sun: Full Body |
|---|---|---|
| **Bench Press** (heavy) | Back Squat (heavy) | **Paused Bench Press** (moderate) |
| **Lat Pulldown** (heavy) | Romanian Deadlift (moderate) | **V-Handle Lat Pulldown** (moderate) |
| **Zanetti Press** 8–12 | Bulgarian Split Squat (moderate) | **Zanetti Press** 8–12 |
| Incline Dumbbell Press 8–12 | Standing Calf Raise 10–15 | Trap Bar Deadlift (heavy) |
| Lateral Raise 12–20 | Tibialis Raise 15–20 | Overhead Press (moderate) |
| External Rotation 15–20 | | Face Pull 15–20 |
| Preacher Curl 10–12 | | Hammer Curl 10–12 |
| | | Reverse Wrist Curl 15–20 |

| Weeks | Heavy lifts | Moderate lifts | Effort |
|---|---|---|---|
| 1–3 | 6–8 | 10–12 | 2 reps short of failure |
| 4 | 6–8 | 10–12 | Lighter week: ~85–90% weights, 3 reps short |
| 5–6 | 5–6 | 8–10 | 1–2 reps short |
| 7–8 | 3–5 | 6–8 | 1–2 reps short, no grinding |

Accessories keep their rep range all 8 weeks and can go to failure. Hit the top of the range on both sets, then add weight next time. Rows and core work are left out on purpose, since gymnastics and climbing cover them. The plan lives in the `PLAN` object at the top of the script.

## Recommended weights

Each exercise shows a *Try* weight × reps, and the form previews it for your first set of that exercise in a workout.

- **Effort logging.** Each set records *reps left in the tank* (0, 1, 2, 3+): one tap, defaulting to the week's effort target. It can be edited later and is shown on each set.
- **Strength estimate.** Every set becomes an estimated max: weight × (1 + (reps + reps left) / 30). Each earlier workout counts its best set, so warm-ups don't drag it down. Light-week workouts are skipped, and the last three workouts are blended 60/25/15, newest first. Sets logged before effort tracking assume their week's target.
- **Prescription.** The weight that lands mid-range at this week's effort target, capped at +10% / −15% of your last top weight and rounded to real plate jumps (5 lb, or 2.5 lb under 50). If that's within one plate step of last time, it keeps your weight and sets the reps instead, moving up a step once you'd reach the top of the range.
- **Beat last time.** If the suggestion is the same weight as last time, it asks for at least one more rep than you did, unless you logged that set at 0 reps left. If that would pass the top of the range, it moves up a plate step instead.
- **Light week (week 4).** About 87% of a normal week's weight, labelled "light week".

| Weeks | Effort target, reps left (heavy & moderate / accessories) |
|---|---|
| 1–3 | 2 / 1 |
| 4 | 3 / 2 |
| 5–8 | 1–2 / 1 |

## The app

- **Log**: shows the next workout in the plan. The form shows your previous set (or a default) as grey preview text; leave a field blank to use it, so repeating a set is one tap on *Add set*. Each exercise shows its target for the current week. Tap *Finish workout* to move on to the next one.
- **Plan**: the 8 × 3 grid (Wed / Fri / Sun) of workouts with finished ones checked off, plus each day's exercises.
- **History**: every session by day. Tap *Edit* on any set to change its weight, reps, exercise or workout, or to delete it.
- **Progress**: estimated one-rep max chart per exercise, heaviest weight, session count. New PRs are flagged.
- **Settings**: lb/kg, export/import a JSON backup.

When it is opened as a Claude artifact, every change is saved on the device first and synced to your Claude account automatically, merging with anything logged on other devices. As a plain file, it lives in that browser's localStorage, so export a backup now and then.
