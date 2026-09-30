# Gym Log

A tiny, single-file workout tracker with a built-in 8-week plan. Open `index.html` in any browser. No build, no server.

## The plan

Supplemental strength work around ~6 h/week of gymnastics and ~3 h/week of climbing. Three gym days, 2 sets per exercise. Bench Press, Lat Pulldown and Zanetti Press are hit twice a week.

| Mon: Legs (after gymnastics) | Fri: Upper (heavy) | Sun: Full Body |
|---|---|---|
| Back Squat (heavy) | **Bench Press** (heavy) | **Paused Bench Press** (moderate) |
| Romanian Deadlift (moderate) | **Lat Pulldown** (heavy) | **Single-Arm Lat Pulldown** (moderate) |
| Bulgarian Split Squat (moderate) | **Zanetti Press** | **Zanetti Press** |
| Standing Calf Raise 10–15 | Incline Dumbbell Press 8–12 | Trap Bar Deadlift (heavy) |
| Tibialis Raise 15–20 | Lateral Raise 12–20 | Overhead Press (moderate) |
| | External Rotation 15–20 | Face Pull 15–20 |
| | Preacher Curl 10–12 | Hammer Curl 10–12 |
| | | Reverse Wrist Curl 15–20 |

| Weeks | Heavy lifts | Moderate lifts | Effort |
|---|---|---|---|
| 1–3 | 6–8 | 10–12 | 2 reps short of failure |
| 4 | 6–8 | 10–12 | Lighter week: ~85–90% weights, 3 reps short |
| 5–6 | 5–6 | 8–10 | 1–2 reps short |
| 7–8 | 3–5 | 6–8 | 1–2 reps short, no grinding |

Accessories keep their rep range all 8 weeks and can go to failure. Hit the top of the range on both sets, then add weight next time. Rows and core work are left out on purpose, since gymnastics and climbing cover them. The plan lives in the `PLAN` object at the top of the script.

## The app

- **Log**: shows the next workout in the plan. The form shows your previous set (or a default) as grey preview text; leave a field blank to use it, so repeating a set is one tap on *Add set*. Each exercise shows its target for the current week. Tap *Finish workout* to move on to the next one.
- **Plan**: the 8 × 3 grid of workouts with finished ones checked off, plus each day's exercises.
- **History**: every session by day. Tap *Edit* on any set to change its weight, reps, exercise or workout, or to delete it.
- **Progress**: estimated one-rep max chart per exercise, heaviest weight, session count. New PRs are flagged.
- **Settings**: lb/kg, export/import a JSON backup.

When it is opened as a Claude artifact, every change is saved on the device first and synced to your Claude account automatically, merging with anything logged on other devices. As a plain file, it lives in that browser's localStorage, so export a backup now and then.
