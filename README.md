# Homebrew tap for kong-harnesses

Use this Homebrew tap to install `kong-harnesses` on macOS or Linux. Homebrew downloads the archive from the [public Kong package repository](https://cloudsmith.io/~kong/repos/kong-harnesses/packages/) and verifies its SHA-256 checksum.

GoReleaser generates the formula for each release. Make future formula changes in the release configuration.

## Install

```sh
brew trust --tap kong/kong-harnesses
brew install kong/kong-harnesses/kong-harnesses
```

## Upgrading from agent-auth-cli

The tool was called `agent-auth-cli`, and this tap was
`Kong/homebrew-agent-auth-cli`. A tap added as `kong/agent-auth-cli` keeps
working, because GitHub sends the old address to this repository.
`formula_renames.json` maps the old formula name to `kong-harnesses`, so
`brew update` and `brew upgrade` move an `agent-auth-cli` install to the new
formula, and `brew install agent-auth-cli` installs `kong-harnesses`. From
v0.9.0 the formula also installs `agent-auth-cli` as a link to
`kong-harnesses`, so client settings that an older release wrote keep working.

To update an old client configuration, run `kong-harnesses profile activate <profile>` for that profile.

Keep the name `homebrew-agent-auth-cli` free in the Kong organization: a new
repository with that name would end the redirect.
