# 🔍 Lab Monitor (Pushover + GitHub Actions)

This repository monitors external URLs (e.g. your homelab services) and sends alerts via [Pushover](https://pushover.net) if any of them go down.

## ✅ How It Works

- Every 5 minutes, GitHub Actions runs a workflow that:
  - Checks a list of URLs (e.g. https://woodpecker.dvirlabs.com)
  - If the status code is 502 or 404, sends an alert via Pushover

## 🔐 Setup

1. Create a free [Pushover](https://pushover.net) account.
2. Get your **User Key** and **App Token**.
3. Go to your repo → Settings → Secrets → Actions → Add these:
   - `PUSHOVER_USER` = your user key
   - `PUSHOVER_TOKEN` = your app token

## 🧪 Test

Temporarily change the URL to something invalid and watch for a Pushover alert.

---
Powered by GitHub Actions 🌀
