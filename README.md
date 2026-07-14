# hawkbit-cli AUR packaging

Arch Linux packaging for [`hawkbit-cli`](https://github.com/pffmachado/hawkbit-cli).

## Package contents

- `PKGBUILD`
- `.SRCINFO`
- GitHub Actions workflows for validation and publish automation

## Build locally

```bash
makepkg -si
```

## Update for a new release

1. Bump `pkgver` in `PKGBUILD`.
1. Regenerate `.SRCINFO`:

```bash
makepkg --printsrcinfo > .SRCINFO
```

3. Commit and push the changes to the AUR git repository.

## Publish workflow

The repository includes a workflow skeleton for automated publishing to AUR using SSH.
Set these secrets in GitHub:

- `AUR_SSH_PRIVATE_KEY`
- `AUR_SSH_KNOWN_HOSTS`

Then run the publish workflow manually from the Actions tab.
