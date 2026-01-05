# Development Guide

This guide is for Doom Emacs. Please refer to the [MELPA contributing guidelines](https://github.com/melpa/melpa/blob/master/CONTRIBUTING.org) for more information.

## Local Installation

In your `packages.el`:

```elisp
(package! magit-pre-commit
  :recipe (:local-repo "/path/to/magit-pre-commit.el" :build (:not compile)))
```

Then run `doom sync`.

## Reloading Changes

### If autoloads change

If you add or modify `;;;###autoload` cookies:

```
M-x doom/reload
```

### For other changes

For most changes, you can simply reload the library:

```
M-x load-library RET magit-pre-commit RET
```

Or evaluate the buffer directly with `M-x eval-buffer` when viewing `magit-pre-commit.el`.
