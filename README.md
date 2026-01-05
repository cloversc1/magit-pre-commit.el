# Magit-pre-commit.el

Magit integration for [pre-commit](https://pre-commit.com/), the framework for managing multi-language pre-commit hooks.

## Installation

### Doom Emacs

In your `packages.el`:

```elisp
(package! magit-pre-commit
  :recipe (:host github :repo "DamianB-BitFlipper/magit-pre-commit.el"))
```

In your `config.el`:

```elisp
(use-package! magit-pre-commit
  :after magit)
```

### Vanilla Emacs

```elisp
(use-package magit-pre-commit
  :ensure t
  :after magit)
```

## Keybindings

From `magit-dispatch` (e.g. `C-x g` then `?`), press `%` to access the pre-commit menu:

| Key | Action                      |
|-----|-----------------------------|
| `r` | Run on staged files         |
| `a` | Run on all files            |
| `h` | Run specific hook           |
| `i` | Install hooks               |
| `u` | Update hooks (autoupdate)   |
| `k` | Kill running process        |

## Key Features

- **Top-level magit integration** - Access pre-commit directly from `magit-dispatch` with `%`
- **Run hooks selectively** - Run on staged files, all files, or a specific hook
- **Hook completion** - When running a specific hook, get completion from your `.pre-commit-config.yaml`
- **Status section** - See running/failed status directly in `magit-status` buffer
- **Auto-activation** - Menu appears only when `pre-commit` is available and config exists
- **ANSI color support** - Pre-commit output rendered with proper colors

## Commands

- `magit-pre-commit` - Open the pre-commit transient menu
- `magit-pre-commit-run` - Run pre-commit on staged files
- `magit-pre-commit-run-all` - Run pre-commit on all files
- `magit-pre-commit-run-hook` - Run a specific hook (with completion)
- `magit-pre-commit-install` - Install pre-commit hooks into git
- `magit-pre-commit-autoupdate` - Update hooks to latest versions
- `magit-pre-commit-kill` - Kill a running pre-commit process
