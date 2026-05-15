# Setup Blueprint

Automated development machine setup using [Blueprint](https://github.com/anomalyco/blueprint).

## Usage

```bash
blueprint apply https://github.com/elpic/setup.git
```

## What Gets Installed

### Terminal & Shell
- **WezTerm** — GPU-accelerated terminal emulator
- **Zsh** + **Oh My Zsh** + **Antigen** — shell with plugin management
- **sesh** + **zoxide** — session management and smart directory jumping
- **tmux** (via mise) + **tpm** — terminal multiplexer with plugin manager

### AI Tools
- **opencode** — AI coding agent built for the terminal, supporting multiple AI providers

### Developer Tools

**Via mise (version-pinned):**
- `sqlite@3.51.2` — embedded SQL database
- `bun@1.3.10` — JavaScript runtime, bundler, and package manager
- `neovim@0.11.1` — extensible text editor
- `tmux@3.6a` — terminal multiplexer
- `fzf@0.53.0` — fuzzy finder
- `ripgrep@15.0.0` — fast recursive search
- `jq@1.8.1` — JSON processor
- `github-cli@2.87.2` — GitHub CLI

**Via Homebrew:**
- `bat` — syntax-highlighted `cat` replacement
- `duf` — modern `df` replacement
- `entr` — run commands on file changes
- `fdupes` — duplicate file finder
- `hyperfine` — command benchmarking
- `procs` — modern `ps` replacement
- `tre` — modern `tree` replacement with editor integration
- `tldr` — simplified man pages with examples
- `htop` — interactive process viewer
- `ncdu` — ncurses disk usage analyzer
- `tree` — directory tree viewer
- `diff-so-fancy` — readable git diffs
- `gum` — interactive CLI components
- `readline` — line-editing library (macOS)
- `pinentry-mac` — GPG passphrase dialog (macOS)
- `rtk` — CLI proxy that reduces LLM token consumption
- **OrbStack** — lightweight Docker Desktop alternative (macOS)
- **Nerd Fonts** — patched fonts with icons for terminal use

### Desktop Apps (macOS / Linux)
- **Slack** — team messaging
- **Brave Browser** — privacy-focused browser
- **Bitwarden** — open-source password manager
- **Rectangle** — window management with keyboard shortcuts (macOS)
- **Postman** — API development and testing
- **TablePlus** — database GUI client (macOS)
- **Notion** — notes, docs, and project management
- **Skitch** — screenshot and annotation tool (macOS)
- **Rewind** — searchable screen and audio recorder (macOS)

### Personal Tools
- **WhatsApp** — messaging
- **Telegram** — messaging
- **Calibre** — e-book manager and converter
- **Hazelnut** — automated file organizer for the terminal (macOS)

### Entertainment
- **Plex Media Server** (Linux)

### System
- SSH key and authentication configuration
- Dotfiles setup
- Passwordless sudo for current user (Linux)
- Daily auto-update schedule (Linux)

## Requirements

- macOS or Linux
- [Blueprint CLI](https://github.com/anomalyco/blueprint) installed
- Internet connection

## Structure

```
setup.bp                  # Main entrypoint
ssh.bp                    # SSH configuration
terminal.bp               # Terminal and shell setup
dotfiles.bp               # Dotfiles management
personal-tools.bp         # Messaging and personal apps
desktop-tools.bp          # Desktop applications
ai/setup.bp               # AI tools
development-tools/
  setup.bp                # Developer tools and runtimes
  nerd-fonts.bp           # Nerd Fonts installation
entertainment/
  setup.bp                # Entertainment (Plex)
```
