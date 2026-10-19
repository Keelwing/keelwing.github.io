# Naming

Decided 2026-10-19, when the projects moved into the organization.

## Repositories

- The organization's own repositories: `.github`, `.github-private`, `keelwing.github.io`; shared CI and build
  images later as `ci` and `sdk-images`.
- A project's repositories carry the project's name, alone or as a prefix: `seaglass`; `sailyard`,
  `sailyard-sessions`, `sailyard-runtime`, `sailyard-plasma`, `sailyard-phosh`.
- A project of several repositories has an umbrella under its plain name (`sailyard`): the docs, the
  architecture, the brand, and each component as a submodule, pinned at a tag that was tested on a phone. The
  submodules have relative URLs (`../<name>.git`) and short paths (`sessions/`, `runtime/`, `plasma/`, `phosh/`).
- Every repository stays private until its project's first public release.

## On the phone

Everything on the phone is in one shared namespace, so the project's name is the prefix there too:

- packages: `seaglass`; Sailyard ships one package, `sailyard` (the app and the per-user sessions), which installs
  the shells' releases;
- systemd units, `/etc/<project>/`, `/usr/share/<project>/`, dconf `/apps/<project>/`, data in `/home/.<project>/`;
  one command for root, `<project>`;
- application and D-Bus names for new code: `io.github.keelwing.<Project>`, e.g. `io.github.keelwing.Sailyard`;
  a project that already has its own keeps it.

## Renaming what already exists

A rename on the phone goes into a release of its own, tested on a phone: the package lists the old name in
`Obsoletes:` and `Provides:`, settings move to the new path on the first start, and old environment variables and
commands stay as aliases for a while.
