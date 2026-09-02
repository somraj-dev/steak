# 🔥 Automated GitHub Streak Keeper

[![Automated Streak Keeper](https://github.com/somraj-dev/steak/actions/workflows/daily-commit.yml/badge.svg)](https://github.com/somraj-dev/steak/actions/workflows/daily-commit.yml)

An intelligent, automated GitHub Actions workflow designed to maintain your GitHub contribution graph and streak with **natural, randomized activity patterns**.

---

## 🎲 Randomized & Natural Activity Features

1. **Random Daily Frequency (2 to 5 Commits/Day):**
   - Each day, the streak engine automatically picks a random target quota (2, 3, 4, or 5 commits).
   - Streak safety is guaranteed: if the day is nearing its end and the target is not yet met, the engine ensures commits execute so your streak is never broken.

2. **Unpredictable & Randomized Timestamps:**
   - Triggers are scheduled across 8 distributed windows (every 3 hours: `01:17`, `04:17`, `07:17`, `10:17`, `13:17`, `16:17`, `19:17`, `22:17 UTC`).
   - Each scheduled run applies a **random sleep jitter (30s – 15min)**, ensuring commits occur at varied, organic minutes and seconds throughout the day rather than fixed clock hours.

3. **Smart State Tracking:**
   - Tracks daily progress in [`activity_state.json`](file:///c:/Users/HP/TDS-action/activity_state.json) and logs current status in [`last_run.txt`](file:///c:/Users/HP/TDS-action/last_run.txt).
   - Generates diverse, realistic commit messages.

4. **On-Demand Manual Trigger:**
   - Can be triggered anytime via GitHub Actions **Workflow Dispatch** for an immediate streak update.

---

## 📋 Essential GitHub Account Setup

For commits made by GitHub Actions to count towards your profile streak and contribution graph:

### 1. 📧 Email Associated with GitHub Account
GitHub credits commits strictly by author email:
- Go to [GitHub Email Settings](https://github.com/settings/emails).
- Ensure your email (`iitainsomraj701@gmail.com`) is listed and **verified**.

### 2. 🔐 Workflow Write Permissions
1. Go to this repository's **Settings** -> **Actions** -> **General**.
2. Scroll down to **Workflow permissions**.
3. Select **Read and write permissions** and click **Save**.

### 3. 👁️ Contribution Graph Visibility (For Private Repos)
If this repository is private:
1. Go to your [GitHub Profile Settings](https://github.com/settings/profile).
2. Under **Contributions & Activity**, check **Include private contributions on my profile**.

---

## 🚀 Manual Run
To manually trigger a commit right now:
1. Go to the [Actions tab](https://github.com/somraj-dev/steak/actions/workflows/daily-commit.yml).
2. Click **Automated Streak Keeper** in the left sidebar.
3. Click **Run workflow** -> Select `main` -> Click **Run workflow**.

---

## 📄 Activity Record
- View the latest human-readable status in [`last_run.txt`](file:///c:/Users/HP/TDS-action/last_run.txt).
- View structured progress history in [`activity_state.json`](file:///c:/Users/HP/TDS-action/activity_state.json).
