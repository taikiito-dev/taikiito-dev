## Taiki Ito

Petroleum trading is my job. I don't write code — I decide what to build and
why, and I build it with [Claude Code](https://claude.com/claude-code).

This account sat empty until August 2026. Everything here started then.

---

### Where this runs

Since September 2026 my photos, files, calendars, passwords and mail have run
on one server I pay for. Most of what is here exists because moving off a
cloud service left a gap.

It is also why the bugs below were findable: a VPS, in Docker, not on a Mac, up
for weeks at a time, in Japanese. A laptop never reaches them.

### Backups

The machine holding my data is also the most likely thing to lose it, so the
offsite copy is deliberately not fully reachable from it. The credential the
server carries can write and delete; it cannot stop replication, rewrite
retention or purge history. A second copy keeps versions the first no longer
has, and does not replicate deletions.

Two things only an audit found, both worth more than the setup itself:

- **A backup log cannot tell you what you forgot.** "33 of 33 OK" only says
  the 33 steps I wrote passed. A service missing from the script fails
  silently, forever, and no log will ever mention it. Coverage has to be
  counted from three directions at once — containers, system services, data
  directories — because each one is blind to what the others hold. A monthly
  job does that now and speaks up only when something is uncovered.
- **Data restores; a machine doesn't.** The first audit found every byte of
  photos, files and mail covered, and not one of the unit files, cron tables or
  firewall rules that say how any of it starts. Everything would have come
  back, with nothing to start it. Those are in the backup now.

Restores are tested rather than assumed — pulled back from the offsite copy and
compared file by file, including through the encrypted path, where even the
directory names are unreadable from the provider's side.

Which software, how it is put together, and the decisions behind all of it —
including the wrong ones — are at **[taikiito.com](https://taikiito.com/)**.

### What I've built

| | |
|---|---|
| **[booking-to-caldav](https://github.com/taikiito-dev/booking-to-caldav)** | Turns booking confirmation emails into events on your own CalDAV server. Watches IMAP over IDLE, so it reacts within seconds instead of polling. Running in production. |
| **[singlish-lah](https://github.com/taikiito-dev/singlish-lah)** · [site](https://singlish.taikiito.com) | A glossary of Singlish and local slang I actually ran into, written for Japanese speakers living here. |

### What I've reported upstream

Six issues on [receptron/mulmoclaude](https://github.com/receptron/mulmoclaude/issues?q=is%3Aissue+author%3Ataikiito-dev).
Four led to fixes:

- [#3415](https://github.com/receptron/mulmoclaude/issues/3415) — journal session links pointed at the wrong path, dead in editors
- [#3357](https://github.com/receptron/mulmoclaude/issues/3357) — the stdio→HTTP shim leaked one port per turn; the MCP server silently disappeared after ~20 turns
- [#3018](https://github.com/receptron/mulmoclaude/issues/3018) — a manually-registered stdio MCP server never surfaced
- [#2937](https://github.com/receptron/mulmoclaude/issues/2937) — intervals over 24h all collapsed into "every day at 00:00 UTC"

Different vantage point, different bugs.

### Writing

Decision records from the move described above, including the calls that turned
out wrong. Mostly in Japanese.

→ [taikiito.com/ja/writing/](https://taikiito.com/ja/writing/)
