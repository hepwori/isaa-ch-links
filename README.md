# isaa-ch-links

Short links for isaa.ch, as a plain text file. Replaces a short.io account.

- **The links live in [`_redirects`](_redirects).** One per line: `/slug  destination  302`.
- **To change one:** edit `_redirects`, push to `main`. Cloudflare Pages redeploys in ~30s. No build step, no code.
- **Use 302, not 301.** Browsers cache 301s more or less forever, so a changed destination wouldn't reach people who'd already clicked.
- **History:** `git log -p _redirects` is the audit trail.
- **Bad syntax** shows up as errors in the Pages deploy log.

Served at `go.isaa.ch`. `/cv` and `/readme` point at the real pages on `isaa.ch` (the homepage repo, `hepwori/isaa.ch`); the apex itself still points at short.io until that homepage is cut over. Full history of the zone is in the `domain-audit` project's tracker.
