## Taiki Ito

Petroleum trading is my job. I don't write code — I decide what to build and
why, and I build it with [Claude Code](https://claude.com/claude-code).

This account sat empty until August 2026. Everything here started then.

→ **[taikiito.com](https://taikiito.com/)**

---

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

These came out of running the thing somewhere it wasn't designed for: a VPS, in
Docker, not on a Mac, up for weeks at a time, in Japanese. Different vantage
point, different bugs.

### Writing

Decision records from moving my photos, files, passwords, mail and calendar off
other people's servers and onto my own — including the calls that turned out
wrong. Mostly in Japanese.

→ [taikiito.com/ja/writing/](https://taikiito.com/ja/writing/)
