# Homebrew tap for kong-harnesses

Use this Homebrew tap to install `kong-harnesses` on macOS or Linux. Homebrew downloads the archive from the [public Kong package repository](https://cloudsmith.io/~kong/repos/kong-harnesses/packages/) and verifies its SHA-256 checksum.

GoReleaser generates the formula for each release. Make future formula changes in the release configuration.

## Install

```sh
brew trust --tap kong/kong-harnesses
brew install kong/kong-harnesses/kong-harnesses
```
