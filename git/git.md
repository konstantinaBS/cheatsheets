## Temporary patches (e.g. for local runs)

Made local changes that you want to apply when working locally but don't want to affect your remotes?

- Create a patch file for the changes you want using `git diff > some.patch`.
- Revert those changes
- Use `git apply some.patch` when you want to work locally
- Use `git apply some.patch --reverse` before you commit

This is equivalent to using shelves in intellij


## Reduce repo size (safe)

```
git reflog expire --all --expire=now
git gc --prune=now --aggressive
```
