# Gym Log

A tiny, single-file workout tracker with a built-in 8-week plan. Open `index.html` in any browser. No build, no server.

## The plan

Upper/lower split, 4 days a week (Mon / Tue / Thu / Fri), 2 sets per exercise. Bench Press, Lat Pulldown and Zanetti Press are on both upper days.

| Upper A | Lower A | Upper B | Lower B |
|---|---|---|---|
| Bench Press | Back Squat | Bench Press | Trap Bar Deadlift |
| Lat Pulldown | Romanian Deadlift | Lat Pulldown | Bulgarian Split Squat |
| Zanetti Press | Leg Press | Zanetti Press | Leg Extension |
| Seated Cable Row | Lying Leg Curl | Seated Dumbbell Shoulder Press | Seated Leg Curl |
| Lateral Raise | Standing Calf Raise | Chest-Supported Row | Hip Thrust |
| Triceps Pushdown | Hanging Leg Raise | Face Pull | Seated Calf Raise |
| EZ-Bar Curl | | Hammer Curl | Cable Crunch |

| Weeks | Reps | Effort |
|---|---|---|
| 1–3 | 10–12 | Stop 2 reps short of failure |
| 4–6 | 8–10 | Stop 1–2 reps short of failure |
| 7–8 | 6–8 | Last set to 0–1 reps short of failure |

Hit the top of the rep range on both sets, then add weight next time. The plan lives in the `PLAN` object at the top of the script.

## The app

- **Log**: shows the next workout in the plan. Tap an exercise to load it (with your last weight and reps), then tap *Add set*. Tap *Finish workout* to move on to the next one.
- **Plan**: the 8 × 4 grid of workouts with finished ones checked off, plus each day's exercises.
- **History**: every session by day.
- **Progress**: estimated one-rep max chart per exercise, heaviest weight, session count. New PRs are flagged.
- **Settings**: lb/kg, export/import a JSON backup.

When it's opened as a Claude artifact, data syncs privately to your Claude account. As a plain file, it lives in that browser's localStorage, so export a backup now and then.
