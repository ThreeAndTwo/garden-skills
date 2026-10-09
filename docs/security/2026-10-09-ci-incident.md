# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/garden-skills`
Branch: `main`
Inspected head: `7668c1ff12b88d437891e922cb7cb31cb516a2ec`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/release-skill.yml` — original Git object `6b7b58c22649414da3a71706b4009beffda7df34`.
- `.github/workflows/validate-skills.yml` — original Git object `777bc63805e4899363e886a6c6304c1a33dead9a`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
