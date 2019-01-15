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

## Count lines of code in repo

Count all lines
```
git ls-files | xargs wc -l
```

Count lines of files with certain extension
```
git ls-files | grep '\.py' | xargs wc -l  # python
git ls-files | grep '\.clj' | xargs wc -l  # clojure
```


## Sign your commits

Requires git 2.0.0 and above
```
git config commit.gpgsign true # set locally
git config --global commit.gpgsign true  # set globally
```
source: https://github.com/git/git/commit/2af2ef3c85612946cac3f16143b4875c9f31c4d2
