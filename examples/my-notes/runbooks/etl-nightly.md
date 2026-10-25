# Runbook: nightly ETL (AWS Batch `etl-nightly`)

Last updated: 2026-10-10

- Runs at 02:00 UTC. The alarm `etl-nightly-failed` fires when any job ends FAILED.
- First check the job's CloudWatch log stream for the error.
- `OutOfMemoryError`: resubmit with the `etl-large` job definition (16 GB).
- Database connection timeouts: check RDS status first, and tell Lena if RDS is degraded.
- Never restart more than 3 jobs in one go without asking me.
- If the ETL is not done by 07:00 UTC, post in #data-consumers that dashboards are delayed.
