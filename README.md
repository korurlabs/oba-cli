# Oba CLI

`oba` works with the Oba apps from a terminal. The command path picks the app, for example `oba otak relation list`.

**This repository distributes the Oba CLI. It does not contain its source.**
The source is maintained privately; every release below is built and published
from there automatically.

## Install

Releases support macOS and Linux on amd64 and arm64.

With Homebrew:

```sh
brew install korurlabs/tap/oba-cli
```

The formula is named `oba-cli`; the binary it installs is `oba`. Upgrade with
`brew upgrade oba-cli`.

With the installer:

```sh
curl -sSfL https://github.com/korurlabs/oba-cli/releases/latest/download/install.sh -o oba-install.sh
sh oba-install.sh
```

The installer picks the archive for your system, checks its SHA-256 checksum
against the release's checksums file, and installs `oba` in `/usr/local/bin`
when that is writable, else in `~/.local/bin`. It never calls sudo.
`OBA_INSTALL_DIR="$HOME/bin" sh oba-install.sh` chooses the directory.

Prebuilt archives and a checksums file are attached to every
[release](https://github.com/korurlabs/oba-cli/releases/latest).

## `go install` is not supported

`go install github.com/korurlabs/oba-cli@latest` will not build: this
repository carries no Go source. Use Homebrew, the installer or a direct download.

## Licence

See [LICENSE](LICENSE).
