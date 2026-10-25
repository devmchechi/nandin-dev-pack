# AWS Ops Analyst

An on-call engineer for your AWS workloads. Ask "why did last night's ETL fail?". It looks at the failed AWS Batch jobs and firing CloudWatch alarms, reads their logs, finds the cause with evidence, and proposes a fix. Restarting a job waits for your approval, and it follows your runbook (Settings › Your rules).

Teammates' agents can ask it too (`ops-analysis`). It investigates for them, but only you can approve a restart.

## What it needs

1. **The AWS CLI** on this computer, and an AWS profile in `~/.aws/config` that can read CloudWatch alarms, CloudWatch Logs and AWS Batch. For restarts, it also needs `batch:SubmitJob`. Keys, SSO (`aws sso login`) and `credential_process` profiles all work.
2. **The AWS connector:** in Library › Tools › AWS, choose Install. In Setup, set the **profile** and **region**, then Start. The calls run on this computer under that profile. No credential reaches the agent's container.
3. **Your runbook:** in the agent's **Settings › Your rules**, add your queues, log groups and rules. Updates to this pack keep them.

Docker must be running.

## Example prompts

- "Why did last night's ETL fail?"
- "What alarms are firing?"
- "Look at job 1a2b3c… and tell me if it's safe to restart."
- "How often has etl-nightly run out of memory this week?"

## Capabilities in plain language

| Capability                     | Why                                                           |
| ------------------------------ | ------------------------------------------------------------- |
| Reads alarms, logs, Batch jobs | Investigating, through your AWS profile                       |
| Restarts a failed Batch job    | Only after you approve the exact call                         |
| Changes anything else in AWS   | No                                                            |
| Network                        | None from its container. AWS calls run on your computer       |
