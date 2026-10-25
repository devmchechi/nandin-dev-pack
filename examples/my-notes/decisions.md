# Decisions

- **2026-09-12:** Production deploys only Tuesday to Thursday, 09:00 to 16:00 local time. Exceptions need my approval in #platform.
- **2026-08-30:** Staging is rebuilt from scratch every Sunday. Don't keep anything there you need.
- **2026-07-18:** All new services use the shared Terraform modules. No hand-made AWS resources in `acme-prod`.
