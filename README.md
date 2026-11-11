# FF Autonomous MS-Paint Pipeline — Live Visual Progress Hub

Live Share-Point Dashboard: **https://connorodea.github.io/ff-progress-hub/**

## Overview

Public-safe, sanitized telemetry and visual showcase hub for the **FF Multi-Series MS-Paint Animation Engine (`bls_engine`)** and **`gitamesh` (`nate <-> connor`)** cross-host agent mesh.

- **Auto-Refresh UI:** Polls `progress_data.json` every `30s` with zero-cache headers.
- **Continuous Pipeline Sync:** Updated automatically via `ff-sync-progress` (`sync_progress.py`) whenever:
  - Scheduled episodes finish rendering (`ScheduleQueue.pop_next_queued`)
  - Daily `09:00 AM` audits execute (`ResendAuditor.send_daily_audit`)
  - `ff sync-hub` or `ff produce` runs from CLI
- **Strict Secret Guard:** Pre-commit / pre-push sanitizer and regex scanner blocks tokens, keys, emails, local paths, and private IPs before any git commit or push.
