# dotfiles

chezmoi-managed dotfiles for Martin's Mac + Hetzner dev VPS (`tmprd-dev`).

Bootstrapped 2026-05-09 as part of the cloud-dev-vps migration Task 1.6 (user_martin role).

## Apply

On a fresh box:

```bash
sh -c "$(curl -fsLS get.chezmoi.io)" -- -b /usr/local/bin
chezmoi init --apply https://github.com/leviemartin/dotfiles.git
```

## Files

- `dot_zshrc` → `~/.zshrc`
- `dot_tmux.conf` → `~/.tmux.conf`
- `dot_gitconfig.tmpl` → `~/.gitconfig` (chezmoi-templated)
- `private_dot_ssh/config` → `~/.ssh/config` (mode 0600)

## Public, by design

No secrets here. Secrets live sops-encrypted in the private `dev-vps-infra` repo.
