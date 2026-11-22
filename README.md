# AthleteHub for Claude

AthleteHub is a strength and conditioning app where coaches plan training and athletes log it. This plugin connects Claude to your AthleteHub account so you can ask about your training data and change it in plain language.

## What it adds

- **MCP connector** `athletehub` at `https://app.athletehub.pro/mcp` (Streamable HTTP). You sign in with your AthleteHub account. Claude sees only what your account can see: a coach sees the athletes on their roster, an athlete sees only their own data.
- **Skills**
  - `weekly-load-review` (coaches): a weekly report of session RPE training load, wellness and readiness flags, and workout completion for a group or an athlete. Read-only.
  - `plan-training-week` (coaches): plan or adjust a calendar week. Finds athletes, groups, templates and exercises, then creates, updates, moves, copies or deletes planned workouts and adds matches or meetings.
  - `todays-session` (athletes): find today's workout, log sets, finish it with session RPE, and submit the daily wellness report.

## What it reads and changes

Read tools cover your profile, athletes and groups, calendar workouts, programs, wellness reports, workout feedback, one-rep maxes, exercises, calendar events and training templates.

Write tools let athletes start, log, complete or abandon their own workouts, submit their daily wellness report, and set a starting one-rep max. Coaches can create, update, move, copy and delete planned workouts on their athletes' calendars, manage matches and meetings, and update athlete details. Claude asks you before any call that deletes or replaces data.

The plugin sends requests only to `app.athletehub.pro`. It runs no local code and stores nothing on your computer.

## Install

In Claude Code:

```text
/plugin install athletehub --marketplace piotr-graczyk-dev/athletehub-claude-plugin
```

On claude.ai and in the desktop app you can also add the connector alone: Settings → Connectors → **Add custom connector**, with the address `https://app.athletehub.pro/mcp`. That adds the tools without the skills.

The first time Claude uses AthleteHub it opens a sign-in page. You choose which areas Claude may read or change, and you can disconnect it at any time in AthleteHub under **Account → API access → Connected apps**.

## Requirements

An AthleteHub account with an active plan.

## Support

Help page: https://athletehub.pro/en/support. Email: support@athletehub.pro. Privacy policy: https://athletehub.pro/en/privacy-policy. Terms of service: https://athletehub.pro/en/terms-of-service.

## Licence

MIT, see [LICENSE](LICENSE). The licence covers this plugin (manifest, connector configuration and skills). The AthleteHub service itself is governed by its terms of service.
