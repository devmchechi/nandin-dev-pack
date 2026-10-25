# My responsibilities

Role: Platform Engineering Lead, Acme Analytics. Reports to Priya Nair (VP Engineering).
Last updated: 2026-10-15

## I own

- **CI/CD:** the GitHub Actions runners and the deploy pipeline for every service.
- **AWS accounts:** `acme-prod` and `acme-staging` (us-east-1). Cost, access reviews and guardrails.
- **Nightly ETL:** the AWS Batch queue `etl-nightly` and its alarms.
- **On-call rota:** for the platform team (6 engineers, weekly rotation, handover on Mondays).

## I don't own (send these on)

- Customer data deletion requests: Data Protection (privacy@acme.example).
- Laptops and SaaS licences: IT helpdesk.
- The billing service: Payments team (lead: Tomás Ruiz).

## Recurring duties

| When                  | What                                                |
| --------------------- | --------------------------------------------------- |
| Mondays 10:00         | Ops review: incidents, alarms, on-call handover     |
| Every Thursday        | Approve production deploy windows for the next week |
| By the 5th each month | AWS cost report to Priya                            |
| Quarterly             | IAM access review of both AWS accounts              |
