# aurvote-utils
A set of utilities for managing AUR votes

## Packages
[`aurvote-utils`](https://aur.archlinux.org/packages/aurvote-utils/)

[`aurvote-utils-git`](https://aur.archlinux.org/packages/aurvote-utils-git/)

## aurvote
If necessary, `aurvote` will prompt for authentication. Cookies are saved in `$XDG_DATA_HOME/aurvote-utils/cookie`
and are renewed automatically. Alternatively, you may regenerate the cookie manually:

```
$ aurvote -a
```

A list of currently voted AUR packages can be queried:
```
$ aurvote -l
```

AUR Package(s) can be voted for:
```
$ aurvote -v foo
$ aurvote -v bar baz
```

And vote(s) can be removed:
```
$ aurvote -u package
$ aurvote -u otherpackage anotherpackage
```

## aurvote-auto
If you wish to show appreciation for the packages you have installed, `aurvote-auto` is the right tool for the job.
When executed, it will vote for installed packages and remove votes for packages that aren't installed.

By default packages that don't belong to a repository are queried.
However, if you use a repository to manage AUR packages (e.g. through `aurutils`), it can be used instead:

```
aurvote-auto -r repo
```
