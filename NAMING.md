# Naming (a proposal)

Not decided yet; this is the starting point for the move of the projects into the organization.

## Repositories

- The organization's own repositories: `.github`, `.github-private`, `keelwing.github.io`; shared CI and build
  images later as `ci` and `sdk-images`.
- A project's repositories carry the project's name, alone or as a prefix: `seaglass`; `sailyard`,
  `sailyard-sessions`, `sailyard-plasma`, `sailyard-phosh`, `sailyard-runtime`.

## On the phone

Everything on the phone is in one shared namespace, so the project's name is the prefix there too:

- packages: `seaglass`, `sailyard-sessions`, `sailyard-plasma`, …
- systemd units, `/etc/<project>/`, `/usr/share/<project>/`, dconf `/apps/<project>/`
- application and D-Bus names for new code: `io.github.keelwing.<Project>`; a project that already has its own keeps
  it.

## Renaming what already exists

A rename on the phone goes into a release of its own, tested on a phone: the package lists the old name in
`Obsoletes:` and `Provides:`, settings move to the new path on the first start, and old environment variables and
commands stay as aliases for a while.
