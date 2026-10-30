# Chief of Staff

Your representative on your team. Teams get work done by finding who is responsible for something, asking them, handing them work and following up. Chief of Staff does that with you, and answers for you when other people ask.

- **"Who's responsible for the SOX audit?"** It searches, live, what everyone connected to your Nandin relay publishes about themselves: their responsibilities, profile and agents. It says who matched, why, and whether they're online.
- **"Who can review my PR on vaultdb?"** It finds people whose responsibilities mention vaultdb and who have a review agent, and offers to send the PR to one of them or to all of them.
- **"Ask Lena for the SOC 1 evidence by Friday."** It finds Lena and writes the request. After you approve, it sends the request to Lena's Nandin, where her Chief of Staff answers or holds it for her.
- **"What am I waiting on?" / "What did people ask me?"** It lists open requests both ways, with status.
- **"Assign Sam: rotate the CI deploy keys, due Friday."** After you approve, it's on Sam's list: Sam's Inbox shows it with the due date until it's marked Done (Sam's note comes back to you) or Declined. You don't wait for it, and it lasts for days, even if one of you goes offline.
- **Questions about you.** When a teammate's agent asks "what does Dev own?", your Chief of Staff answers from your role and notes. Work someone assigns you waits for your approval, then stays in your Inbox until you click Done or Decline.
- **Questions about your own work** ("What's due this week?") are answered from your notes, with sources.
- **It keeps your notes.** Say hello and it gets to know you: a few questions about your role, what you own, what's due and who you work with, organized into notes you can read and edit on the **My notes** page. After that, tell it things as they happen ("the walkthrough moved to Nov 19") and it files them, then points out what's coming up or overdue. Work others assign you goes into your notes too: at the start of a chat it checks your list and notes what's new, done or declined.
- **When it acts.** Only when you chat with it, a teammate asks it something, or a trigger you set up messages it. It doesn't watch in the background. For a daily check-in, add a schedule trigger (for example weekdays at 9:00: "What needs my attention today?").

## Set it up

1. **Your role.** Open the agent's **Settings › Your rules** and fill them in: title, team, what you own, recurring duties and who to escalate to. Updates to this pack keep them.
2. **Your responsibilities, so others can find you.** In your `NANDIN.md` (Settings › Gateway, or the file in your agents repo), list them:
   ```yaml
   responsibilities: [CI/CD, AWS accounts, on-call rota, SOX IT controls]
   policy:
     require_approval: [assign-me]   # work assigned to you waits for you
   ```
   Your Nandin publishes these with your profile on the relay.
3. **Be reachable.** Turn the gateway on and connect to your team's relay. To share your `NANDIN.md` text as well, make your profile discoverable.
4. **Your notes.** Open **My notes**: Nandin creates your notes folder and shares it with Chief of Staff. Keep **Let Chief of Staff keep them up to date** on so it can file what it learns without asking each time. To try it with sample notes, copy `examples/my-notes/` into that folder.

Docker must be running.

## Example prompts

- "Who is responsible for Risk?"
- "List everyone on my network and what they own."
- "Who can review my pull request on vaultdb?" then "Ask all of them" or "Ask whoever is online."
- "Ask the SOC 1 owner for last quarter's evidence."
- "Assign Sam: rotate the CI deploy keys, due Friday."
- "What am I waiting on?"
- "What's due this week?"

## Capabilities in plain language

| Capability                       | Why                                                                                            |
| -------------------------------- | ---------------------------------------------------------------------------------------------- |
| Reads your network's profiles    | Finding who is responsible, from what people publish on your relay                             |
| Sends requests (asks first)      | Asking people and assigning work, each request approved by you                                 |
| Answers for you                  | Questions about your work (`ask-me`). Work assigned to you (`assign-me`) waits for your approval, then for your Done or Decline |
| Reads and keeps your notes       | The `my-notes` folder. It writes there only while My notes allows it, without asking each time  |
| Writes files or runs commands    | No                                                                                             |
