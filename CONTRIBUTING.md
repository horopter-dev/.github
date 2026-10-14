# Contributing

These are the rules every repository in the horopter-dev organisation shares. A repository
with its own `CONTRIBUTING.md` adds to them: how to set it up and which checks to run before
you open a pull request.

## Sign-off

There is no CLA. Instead, every commit must carry a `Signed-off-by` line certifying the
Developer Certificate of Origin, reproduced in full below:

    git commit -s -m "fix: link the install guide from the home page"

`-s` appends the line using your configured `user.name` and `user.email`, so both must be set
to a real name and a reachable address:

    Signed-off-by: Jane Doe <jane@example.com>

The [DCO app][dco-app] checks every pull request and fails one whose commits are not all
signed off. Bots and merge commits are excluded. If you forgot, add the line to every commit
on your branch and force-push it:

    git rebase --signoff main
    git push --force-with-lease

### Developer Certificate of Origin 1.1

```
Developer Certificate of Origin
Version 1.1

Copyright (C) 2004, 2006 The Linux Foundation and its contributors.

Everyone is permitted to copy and distribute verbatim copies of this
license document, but changing it is not allowed.


Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

## Pull requests

Pull requests are squash-merged; it is the only merge button. The squash commit takes the
pull request's title as its subject, so the title is what lands on `main`. Write it in
[Conventional Commits][cc] form, in the imperative mood and under 72 characters:

    fix: stop the theme toggle flashing on load
    docs(how-to): add the Flux walkthrough

Where a repository is released by Release Please, that line is also its changelog entry and
its type picks the next version, so keep each pull request to one change.

[cc]: https://www.conventionalcommits.org/en/v1.0.0/
[dco-app]: https://github.com/apps/dco
