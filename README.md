# to11-cli

Company skills for your coding agent.

A **skill** is a folder of files your agent reads — a runbook, a house style, a
review checklist. `to11` keeps the ones your company publishes current on your
machine, and lets a maintainer store and release a version without opening a
browser.

This repository hosts the releases. The source lives elsewhere.

## Install

```bash
brew install to11ai/tap/to11
```

### With asdf

Requires [asdf](https://asdf-vm.com) 0.16 or newer.

```bash
asdf plugin add to11 https://github.com/to11ai/asdf-to11
asdf install to11 latest
asdf set to11 latest
```

### By hand

Download the archive for your platform from the
[latest release](https://github.com/to11ai/to11-cli/releases/latest), then put the
`to11` binary somewhere on your `PATH`.

## Verify

```bash
to11 --version
```
