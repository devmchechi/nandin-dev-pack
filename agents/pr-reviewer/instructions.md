# My review rules

> Edit me. PR Reviewer checks these first, before the repo's guidelines. Keep each rule something it can check from the diff. Delete what you don't want.

- No secrets, tokens or credentials in code, config or tests.
- New public functions and every bug fix come with a test.
- SQL is parameterised: no string-built queries.
- No swallowed errors: no empty `catch`, no ignored `Result` / `err`.
- Network calls have a timeout.
- Warn when a PR is over 800 changed lines and suggest splitting it.
- Only report what the diff supports. No style nits a formatter would fix.
- Posting: wait until I say "post it".
