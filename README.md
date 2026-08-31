# 🔥 Automated GitHub Streak Keeper

[![Automated Streak Keeper](https://github.com/somraj-dev/steak/actions/workflows/daily-commit.yml/badge.svg)](https://github.com/somraj-dev/steak/actions/workflows/daily-commit.yml)

An automated GitHub Actions workflow designed to maintain your GitHub contribution graph and streak consistently and reliably.

---

## ⚙️ How It Works

1. **Scheduled Triggers:** The workflow runs automatically **twice daily** (at `04:00 UTC` and `16:00 UTC` / `09:30 AM` and `09:30 PM IST`) to ensure timezone coverage and prevent missed days from GitHub Actions queue delays.
2. **On-Demand Trigger:** Can be manually triggered at any time via the **Actions** tab (`workflow_dispatch`).
3. **Commit Generation:** Updates [`last_run.txt`](file:///c:/Users/HP/TDS-action/last_run.txt) with a clean activity timestamp and pushes back to `main`.

---

## 📋 Essential GitHub Account Setup (Must-Check)

For commits made by GitHub Actions to count towards your profile streak and contribution graph, ensure the following 3 settings are configured:

### 1. 📧 Email Associated with GitHub Account
GitHub credits commits strictly by the **author email**.
- Go to [GitHub Email Settings](https://github.com/settings/emails).
- Ensure your email (`iitainsomraj701@gmail.com`) is listed and **verified**.
- *Optional:* You can also set custom author details in this repository under **Settings > Secrets and variables > Actions**:
  - `GIT_USER_NAME`: `somraj-dev`
  - `GIT_USER_EMAIL`: `iitainsomraj701@gmail.com`

### 2. 🔐 Workflow Write Permissions
GitHub Actions must have permission to push commits to this repository:
1. Go to this repository's **Settings**.
2. Navigate to **Actions** -> **General**.
3. Scroll down to **Workflow permissions**.
4. Select **Read and write permissions**.
5. Click **Save**.

### 3. 👁️ Contribution Graph Visibility (For Private Repos)
If this repository is private:
1. Go to your [GitHub Profile](https://github.com/).
2. Click **Edit profile** (or your profile settings).
3. Under **Contributions & Activity**, check **Include private contributions on my profile**.

---

## 🚀 Manual Run
To manually test or trigger the workflow right now:
1. Go to the [Actions tab](https://github.com/somraj-dev/steak/actions/workflows/daily-commit.yml).
2. Click **Automated Streak Keeper** in the left sidebar.
3. Click the **Run workflow** dropdown button on the right.
4. Select the `main` branch and click **Run workflow**.

---

## 📄 Activity Record
The latest activity status is recorded in [`last_run.txt`](file:///c:/Users/HP/TDS-action/last_run.txt).
