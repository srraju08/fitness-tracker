# 6-Month Transformation Tracker

A one-page tracker for the 26-week plan. Each day you log weight, steps, sleep, protein, calories, cardio, whether you did your session and core work, whether you took whey, and your waist every 2 weeks. It works out weekly averages, draws the charts, and checks your numbers against the plan's calorie-adjustment rules.

Keep logging sets and reps in Hevy. This tracker covers everything Hevy doesn't.

## Setup (about 10 minutes)

### 1. Host the app (public repo)
1. On GitHub, create a **public** repo named `fitness-tracker`.
2. Upload `index.html`, `manifest.json` and `icon.svg`.
3. Go to **Settings → Pages → Build and deployment**, set Source to *Deploy from a branch*, then pick branch `main` and folder `/ (root)`. Save.
4. After about a minute, the app is live at `https://srraju08.github.io/fitness-tracker/`.
5. On your phone, open that link and choose **Add to Home screen**.

The app repo holds code only. None of your numbers go there.

### 2. Store your data (private repo, optional but recommended)
1. Create a **private** repo named `fitness-data`. Tick "Add a README" so the repo isn't empty.
2. Create a token: **GitHub → Settings → Developer settings → Fine-grained tokens → Generate new token**.
   - Repository access: *Only select repositories* → `fitness-data`
   - Permissions → Repository → **Contents: Read and write**
   - Expiry: up to 1 year (put a reminder in your calendar to renew it)
3. In the app, go to **Settings → GitHub sync** and enter owner `srraju08`, repo `fitness-data` and the token. Tick *Push automatically after every save*, then save.
4. Do the same on your PC browser. Every save pushes to `fitness-data/data.json`. If both devices edit the same day, the newer edit wins.

The token stays saved in that browser only. If you lose your phone, delete the token on GitHub.

### Without sync
Your data is saved only in that one browser. Use **Export JSON** every week as a backup.

## How it uses the plan
- **Week 1** is the Monday you set in Settings. The app shows the current phase (Foundation, Development, Deload, Strength, Refinement, Review), today's session, and that day's core and cardio.
- **Calorie rules** kick in once two weeks each have 3 or more weigh-ins:
  - Losing 0.25–0.5 kg a week: change nothing.
  - Weight and waist flat for 3 weeks: cut about 150 kcal a day **or** add walking, not both.
  - Losing faster than 0.75 kg a week for 2 weeks: add 150–200 kcal a day.
  - Weight flat but waist going down: change nothing.
- It also warns you when protein days, sleep or steps fall behind target.
