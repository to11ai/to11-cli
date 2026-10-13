# to11-cli

The agent skill sharing CLI.

Centrally maintain your team's agent skills that sync automatically to every
developer. Scope skills per terminal session to the task at hand and keep
context clean.

A **skill** is a folder of files your agent reads — a runbook, a house style, a
review checklist. `to11` keeps the ones your team publishes current on every
machine, and lets a maintainer release a new version without opening a browser.

This repository hosts the releases. The source lives elsewhere.

## Install

Runs on macOS and Linux (x86-64 and arm64). There is no Windows build yet.

```bash
brew install to11ai/tap/to11
```

### With apt (Ubuntu & Debian)

```bash
sudo apt-get install -y curl gnupg
curl -fsSL https://apt.fury.io/to11/gpg.key | sudo gpg --dearmor -o /usr/share/keyrings/to11-keyring.gpg
sudo chmod go+r /usr/share/keyrings/to11-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/to11-keyring.gpg] https://apt.fury.io/to11/ * *" | sudo tee /etc/apt/sources.list.d/to11.list
sudo apt update
sudo apt install to11
```

### With dnf (Fedora & RHEL)

```bash
sudo rpm --import https://yum.fury.io/to11/gpg.key
sudo tee /etc/yum.repos.d/to11.repo <<EOF
[to11]
name=to11 Repository
baseurl=https://yum.fury.io/to11/
enabled=1
# repo_gpgcheck verifies the signed repo metadata; gpgcheck is 0 because
# the .rpm itself is not individually signed (a separate, unshipped step).
gpgcheck=0
repo_gpgcheck=1
gpgkey=https://yum.fury.io/to11/gpg.key
EOF

sudo dnf install to11
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
