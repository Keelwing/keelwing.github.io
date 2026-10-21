# Naming

Decided 2026-10-19, when the projects moved into the organization; extended 2026-10-21.

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
- systemd units, `/etc/<project>/`, `/usr/share/<project>/`, `/usr/libexec/<project>/`, `/run/<project>/`, dconf
  `/apps/<project>/`, data in `/home/.<project>/`; one command for root, `<project>`;
- environment variables: the prefix `<PROJECT>_`, with sub-prefixes for the package's own keys (Sailyard:
  `SAILYARD_` for the runtime's keys, `SAILYARD_APP_`, `SAILYARD_CLI_` and `SAILYARD_TEST_` for the package's);
- inside a directory only the project writes, names do not repeat the prefix (`/etc/sailyard/users.conf`), except
  the main configuration file, `/etc/<project>/<project>.conf`;
- units are `<project>-<verb>@`, and a project's unit verbs are distinct: one verb, one job, and polkit patterns of
  different verbs that cannot overlap. Where one verb has two instance forms, a reserved word tells them apart.

"Application name" means:

- on Sailfish, the `sailfish-qml` name, `<project>`: the desktop file, `/usr/share/<project>/`, the translations
  and the icon;
- elsewhere, the reverse-DNS id `io.github.keelwing.<Project>[.<Layer>.<Thing>]`, e.g. `io.github.keelwing.Sailyard`,
  used for D-Bus names, Sailjail keys, Wayland app ids and KPackage ids, never for file names. A project that
  already has its own keeps it.

## Renaming what already exists

A rename on the phone goes into a release of its own, tested on a phone. The package lists the old names in
`Obsoletes:` and `Provides:` for good. Settings move to the new path on the first start. Old commands, environment
variables, configuration keys, files and units stay as aliases until a condition the project's `doctor` measures
(a `compat.*` check), and at the latest until the first public release, never by a date.

Two kinds of old names stay for good, and each is listed in `docs/ABI.md` of the repository that owns it, with its
readers:

- **runtime protocol 1:** names compiled into binaries that ship inside a rootfs, persisted in rootfs copies, or
  read by older tools and packages that a phone can still run;
- **rootfs-internal file names:** files the overlay sync or the package writes into a rootfs. A rename there would
  leave both copies.

New code uses the new names. Sailyard's rename is step 6 of
[its migration](https://github.com/Keelwing/sailyard/blob/main/docs/MIGRATION.md).
