# doombringerz-vault

> The Laziest YouTuber's Obsidian setup. ADHD-friendly starter vault. Fork it, work in it, change one thing per week until it's yours.

Made by [Doombringerz](https://doombringerz.com).

## Why

Most Obsidian starter vaults assume you're a neurotypical knowledge worker who wants to recreate Maggie Appleton's digital garden. This one assumes:

- You alternate between "doing absolutely nothing" and "OH BOI does shit get done"
- You forget you've started notes if they don't auto-bubble up somewhere
- You'd rather have a working setup today than spend 8 hours watching tutorials
- You want capture friction to be near zero (the thought goes away fast)
- You want the tool to show you the rhythm of your work, not pretend you're a 9-to-5

It's built around that.

## What's in it

```
doombringerz-vault/
├── .obsidian/                 # pre-enabled plugins + sensible app defaults
├── 00 Inbox/                  # all new notes land here (set in app.json)
├── 01 Daily/                  # daily notes (periodic-notes auto-creates)
├── 02 Weekly/                 # weekly notes (periodic-notes auto-creates)
├── 03 Projects/               # active projects (Example Project shows the shape)
├── 04 Reference/              # long-term notes you'll re-read
├── 99 Archive/                # done / dead / cold storage
├── _templates/                # Templater templates: Daily, Weekly, Project
└── _assets/                   # attachments folder (set in app.json)
```

## Install

1. **Clone or download** this repo to wherever you keep your vaults
   ```powershell
   git clone https://github.com/Doombringerz/doombringerz-vault.git
   ```
2. **Open the folder in Obsidian** ("Open folder as vault")
3. **Install the listed community plugins.** Obsidian will show "22 plugins are not installed" on first open. Click each, install, enable. (Or use the manual list below if you prefer that flow.)
4. **Restart Obsidian** so all plugins activate cleanly
5. **Configure Templater** (Settings, Templater) to use `_templates` as the template folder
6. **Configure Periodic Notes** (Settings, Periodic Notes):
   - Daily notes folder: `01 Daily`
   - Daily template: `_templates/Daily.md`
   - Weekly notes folder: `02 Weekly`
   - Weekly template: `_templates/Weekly.md`

You're done. Hit cmd+P, search "Periodic Notes: Open today's daily note", and you're in.

## The plugin list

Twenty-two, grouped by what they do for you:

### Capture and tasks (the load-bearing ones for ADHD)
- **quickadd**, capture text or a task in one keybind, before the thought escapes
- **obsidian-tasks-plugin**, task management with due dates, recurrence, queries
- **periodic-notes**, daily and weekly notes on a schedule
- **templater-obsidian**, real templates with logic and date math

### Querying and rollups
- **dataview**, query your notes like a database. Powers the Daily and Weekly rollups
- **auto-note-mover**, auto-organize notes based on tags (less manual sorting)

### Visual thinking
- **obsidian-excalidraw-plugin**, drawing canvas. Great for visual thinkers
- **obsidian-kanban**, drag-and-drop task boards
- **obsidian-outliner**, bullet-driven thought
- **cards-view**, browse notes as visual cards instead of file lists

### Time and focus
- **obsidian-day-planner**, time-blocking. Fixes ADHD time-blindness
- **obsidian-hover-editor**, preview any link without leaving your current note

### Visual cues (more visual signal = less re-reading)
- **highlightr-plugin**, color-coded highlighting
- **obsidian-banners**, header images on notes
- **obsidian-icon-folder**, icons on folders for fast scanning
- **colored-tags-wrangler**, color-code your tags
- **tag-wrangler**, rename and merge tags

### Quality of life
- **obsidian-linter**, auto-format on save
- **obsidian-style-settings**, easy theme tweaks
- **workspaces-plus**, switch workspaces fast
- **file-cleaner-redux**, find and remove orphan attachments
- **local-backup**, scheduled local backups (peace of mind)

## How the Daily note works

Every daily note (auto-created from `Daily.md`) starts with:

- **Energy**: low / medium / OH BOI
- **Mode**: deep focus / shallow / admin / rest
- **Top 3 today**, three things you'll do (only three)

Then there are two Dataview queries that auto-fill:

- **What got done today**, every task completed today, across the whole vault
- **Rolled over**, every open task with a due date that's today or earlier

The point: you don't have to manually track. Just write `- [ ] task @due(2026-05-20)` anywhere and it shows up in the right places.

## Customize it

It's yours. Change one thing per week:

- Add or remove plugins
- Edit templates in `_templates/`
- Tweak `.obsidian/app.json` (Inbox folder name, attachment folder, etc)
- Change folder structure to match how YOU work

The starter is opinionated so you have a real starting point. Make it yours over weeks.

## What's NOT in this vault

Deliberately:

- **No personal MCP or integration configs** (set those up per machine if you use any)
- **No custom CSS snippets** (clean default, add your own)
- **No theme** (Obsidian default; install whatever theme you like)
- **No notes from my actual vault** (private)

## License

MIT, see [LICENSE](LICENSE).

## Related

- [doombringerz.com](https://doombringerz.com)
- [oh-boi-cli](https://github.com/Doombringerz/oh-boi-cli), companion ADHD focus tracker
- [win-rice-doombringerz](https://github.com/Doombringerz/win-rice-doombringerz), companion terminal setup
