# Contributing

This is the default contributing guide for `exploopio` repositories that do not
have their own. Most repositories here are private and take changes from the
maintainers only. Open source work happens in [openctemio](https://github.com/openctemio);
contribute there.

## Where to open a pull request

- Base branch: `main`, in every repository.
- Branch names: `<type>/<short-slug>` with `<type>` one of `feat`, `fix`, `docs`,
  `refactor`, `test`, `ci`, `build`, `chore`, `perf`, `security`.
  `release/*` is reserved for the Release Prepare workflow.
- Nothing is pushed straight to `main`; it cannot be force-pushed or deleted.

## Commits

- Conventional Commits (`type(scope): summary`, `type!:` for a breaking change).
- Sign off every commit (`git commit -s`) with your GitHub noreply address.
- No AI or tool attribution: no `Co-Authored-By` trailer naming a tool or
  assistant, no "Generated with" lines, no tool session links. The
  `No AI attribution` check fails on them.
- No secrets, customer identifiers, internal hostnames or private addresses.
  Push protection and the secret scan check enforce it.
- A user-visible change adds `changelog.d/<short-slug>.md` where the repository
  has a `changelog.d/` directory.

## Merging

Every required check passes and every review conversation is resolved. A change
to a path listed in `.github/security-paths.yml` needs the `security-ack` label
from a maintainer before `security-gate` passes; automation never adds it.
Release tags (`v*`) come from the release workflow or a maintainer and are never
moved or deleted.

## Security issues

See [SECURITY.md](SECURITY.md).
