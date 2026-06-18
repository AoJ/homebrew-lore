# homebrew-lore

Private Homebrew tap for [lore](https://github.com/AoJ/lore).

`Formula/lore.rb` and `Casks/lore.rb` are **auto-generated** on each tagged
release by the `homebrew` job in `AoJ/lore`'s `.github/workflows/release.yml`
(rendered from the `tools/homebrew/` templates). Do not hand-edit them here —
edit the templates in the main repo instead.

## Install

The repo is private, so two things are needed once:

```bash
# 1. Tap over SSH (uses your ssh-agent key, no token)
brew tap AoJ/lore git@github.com:AoJ/homebrew-lore.git

# 2. A token with read access to AoJ/lore, for downloading the binaries.
#    Kept separate from any global HOMEBREW_GITHUB_API_TOKEN.
export HOMEBREW_LORE_GITHUB_TOKEN=ghp_...
```

Then:

```bash
brew install --cask lore   # Lore.app desktop GUI (pinnable to the Dock)
brew install lore          # CLI: lore, lore-serve, lore-worker
brew upgrade               # pulls new tagged releases
```

See the main repo's README for details (Gatekeeper, `LORE_DB`, multi-account
token notes).
