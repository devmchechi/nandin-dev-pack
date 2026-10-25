# My runbook

> Edit me. AWS Ops Analyst follows these rules before its defaults. Name your real queues, log groups and limits.

- **What to watch:** the AWS Batch queue `etl-nightly` and the alarms starting with `etl-`.
- **Log groups:** Batch jobs log to `/aws/batch/job`.
- **Out of memory (exit code 137, `OutOfMemoryError`):** a restart is OK once. If it fails again, propose the `etl-large` job definition (16 GB) instead.
- **Database connection timeouts:** don't restart. Tell Lena (database owner) first.
- **Restarts:** at most 3 jobs in one go, never without my approval.
- **Late data:** if the nightly ETL hasn't finished by 07:00 UTC, say that dashboards will be delayed.
- **Never:** delete jobs, change job definitions or queues, or touch production data.
