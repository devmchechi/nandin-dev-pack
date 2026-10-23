# PR Reviewer

Reviews a GitHub pull request against **your** rules first, then the repo's own guidelines (`REVIEW.md`, `CONTRIBUTING.md`, `AGENTS.md`, `CLAUDE.md`). It reports a verdict and findings, most severe first, each with a file and line, the rule it breaks, why it matters and a fix. When you say "post it", it posts the review on the PR as inline comments, after you approve the exact comments.

It works on private repositories. Your GitHub token stays on your computer: the GitHub calls run in Nandin, not in the agent's container.

## What it needs

1. **A GitHub token.** Create a [fine-grained personal access token](https://github.com/settings/personal-access-tokens/new) for the repositories you want reviewed, with the permissions **Contents: Read** and **Pull requests: Read and write**. (Read-only is enough if you never post reviews.)
2. **The GitHub connector.** In Library › Tools › GitHub, choose Install. In Setup, paste the token, then Start.
3. **Your rules.** Open the agent's Instructions tab and edit `instructions.md`.

Docker must be running.

## Example prompts

- "Review https://github.com/acme/web/pull/42"
- "Review acme/web#42 and focus on security."
- "Post it."

## Capabilities in plain language

| Capability               | Why                                                      |
| ------------------------ | -------------------------------------------------------- |
| Reads pull requests      | The PR's diff and files, through your GitHub token       |
| Posts reviews (asks first) | Inline comments on the PR, only after you approve them |
| Writes files             | No                                                       |
| Runs commands            | No                                                       |
| Network                  | None from its container. GitHub calls run in Nandin      |
