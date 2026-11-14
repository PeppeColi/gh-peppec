# gh-peppec

A [gh](https://cli.github.com) extension that runs the command line of
[PEPPEC](https://github.com/PeppeColi/peppec): `init`, `doctor` and `bot`.

```sh
gh extension install PeppeColi/gh-peppec
cd your-host-repo
gh peppec init
```

Each run downloads `cli/peppec` from the engine at the requested version (`v2` by
default, or the one given with `--ref`), so there is nothing to update: `gh peppec`
always runs the current CLI of that version. Without a network it falls back to the
copy it downloaded last time.

Needs gh (signed in), jq, git, curl and openssl. See the engine's
[setup guide](https://github.com/PeppeColi/peppec/blob/main/docs/setup.md) for what
`init` asks and does.

Environment: `PEPPEC_REF` (engine version, default `v2`), `PEPPEC_ENGINE` (engine
repository, default `PeppeColi/peppec`).
