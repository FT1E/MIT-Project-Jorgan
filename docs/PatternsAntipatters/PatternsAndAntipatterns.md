# Project Jorgan — Antipatterns and Patterns

## Antipatterns to Avoid

### 1. Ignore Human Issues

For a two-person team, ignoring personal or interpersonal problems is especially dangerous. If one team member is burned out, stressed about exams, or silently frustrated with how work is divided, the entire project feels it immediately — there's no buffer of 10 other engineers to absorb the slack.

In Project Jorgan this would mean making it a habit to have brief, honest check-ins at the start of each work session. Not just "what did you do?" but "how are you feeling about the project right now?" Since the deadline is August 2026 and the project spans months, fatigue will accumulate. Catching it early — before it turns into resentment or disengagement — is far cheaper than trying to recover a demotivated teammate in the final sprint.

### 2. Treat Your Team Like Children (Infantilization)

On a two-person team where both members are also the clients, this antipattern takes a subtle form: over-supervising or second-guessing each other's technical decisions. If one takes ownership of the Cloudflare networking setup, the other partner constantly questioning every config choice is the equivalent of a manager hovering. It signals a lack of trust and kills motivation. This should actively be avoided and each team member should have equal ownership as well as responsibility.

---

## Positive Patterns to Adopt

### 1. Set Clear Goals

This one is already partially done through the Project Jorgan Charter's milestones, which is a great sign. The pattern is only valuable, however, if the goals remain living checkpoints rather than a document written once and forgotten. For Project Jorgan this means revisiting each milestone at the start of the week it's due — not to add pressure, but to break it into concrete tasks. For example, "Server can be accessed from any device via a browser" (Milestone 4, March 23) should become a short list:

- DNS entry configured
- HTTPS cert obtained via Cloudflare
- Tested on mobile and desktop

Vague milestones cause drift; concrete sub-tasks don't.

### 2. Be a Catalyst (and Remove Roadblocks)

These two are grouped because for a small team they happen simultaneously. Being a catalyst means not waiting for problems to solve themselves — when one team member is stuck on something outside their expertise (say, a MariaDB permission issue), the other doesn't just shrug and say "not my area." You actively unblock each other, even if it means doing a debugging session or spending 30 minutes researching together.

In practical terms for Project Jorgan: agree that if either person is blocked for more than a couple of hours on something, they immediately flag it rather than silently and unsuccessfully working on it alone. A blocked teammate on a two-person project is a 50% productivity loss. Unblocking each other fast is one of the highest-leverage things this team can do.