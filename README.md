# aurvote-utils
A set of utilities for managing AUR votes

## Packages
[`aurvote-utils`](https://aur.archlinux.org/packages/aurvote-utils/)

[`aurvote-utils-git`](https://aur.archlinux.org/packages/aurvote-utils-git/)

## aur-vote
> NOTE: If you have `aurutils` installed, `aur vote` may be used instead.

If necessary, `aur-vote` will prompt for authentication. Cookies are saved in `$XDG_DATA_HOME/aurvote-utils/cookie`
and are renewed automatically. Alternatively, you may regenerate the cookie manually:

```
$ aur-vote -a
```

A list of currently voted AUR packages can be queried:
```
$ aur-vote -l
```

AUR Package(s) can be voted for:
```
$ aur-vote -v foo
$ aur-vote -v bar baz
```

And vote(s) can be removed:
```
$ aur-vote -u package
$ aur-vote -u otherpackage anotherpackage
```

## aur-autovote
> NOTE: If you have `aurutils` installed, `aur autovote` may be used instead.

If you wish to show appreciation for the packages you have installed, `aur-autovote` is the right tool for the job.
When executed, it will vote for installed packages and remove votes for packages that aren't installed.

By default packages that don't belong to a repository are queried.
However, if you use a repository to manage AUR packages (e.g. through `aurutils`), it can be used instead:

```
aur-autovote -r repo
```
