# Ninja Paws Organization Defaults

This repository contains organization-wide defaults for Ninja Paws public
repositories.

GitHub uses specially named `.github` repositories for default community health
files and public organization profile content. Repository-specific files still
take precedence: if a project has its own `CONTRIBUTING.md`, `SECURITY.md`,
issue templates, or pull request template, GitHub uses the local project file
instead of this default.

## Public Notice

Ninja Paws is an independent community and demo organization. The repositories
in this organization are not Microsoft products or GitHub products unless a
repository explicitly says otherwise.

Read the canonical [Ninja Paws disclaimer](DISCLAIMER.md) before relying on any
code, scripts, demos, recommendations, estimates, reports, or deployment assets.

## Files In This Repository

- `profile/README.md` - public organization profile shown on GitHub.
- `DISCLAIMER.md` - canonical disclaimer text for Ninja Paws repositories.
- `ninjapaws-metadata.json` - machine-readable organization metadata for
  repository setup scripts, audits, and documentation checks.
- `CONTRIBUTING.md` - default contribution guidance for repositories without a
  local contribution guide.
- `SECURITY.md` - default vulnerability reporting guidance.
- `SUPPORT.md` - default support and issue routing guidance.
- `CODE_OF_CONDUCT.md` - default community behavior expectations.
- `GOVERNANCE.md` - default project governance model.
- `.github/ISSUE_TEMPLATE/` - default issue forms.
- `.github/PULL_REQUEST_TEMPLATE/` - default pull request template.
- `.github/workflow-templates/` - optional starter workflow templates.

## Recommended Repository Pattern

For public Ninja Paws repositories:

1. Keep a local `LICENSE` file in every repository.
2. Keep a local `DISCLAIMER.md` file in every repository, copied from this
   repository or intentionally adapted for that project.
3. Add a short disclaimer block near the top of each public `README.md` and link
   to `DISCLAIMER.md`.
4. Keep security reports out of public issues. Use GitHub private vulnerability
   reporting where enabled, or follow the repository's `SECURITY.md`.
5. Prefer pull requests for disclaimer updates rather than a workflow that
   silently overwrites legal or policy text across repositories.

## GitHub Default File Notes

GitHub can use this repository for default community health files such as
`CONTRIBUTING.md`, `SECURITY.md`, `SUPPORT.md`, `CODE_OF_CONDUCT.md`, issue
templates, and pull request templates.

GitHub does not treat `DISCLAIMER.md`, `LICENSE`, `CODEOWNERS`, or
`dependabot.yml` as organization-wide default files. Add those files directly to
each repository when they are required.

## Metadata and Sync Guidance

Use `ninjapaws-metadata.json` as a small machine-readable source of truth for
copyright holder, license SPDX ID, disclaimer version, support posture, and
official-status flags. This is useful for repo audit scripts and PR checks, but
it is not a GitHub-native policy mechanism.

Recommended sync model:

- Use explicit pull requests to update local `DISCLAIMER.md`, `LICENSE`,
  `CODEOWNERS`, and `dependabot.yml` files.
- Use a lightweight audit workflow or script to report drift from the canonical
  metadata and disclaimer.
- Avoid workflows that silently overwrite policy, license, or legal text across
  repositories.

Security and dependency automation is best handled through repository settings,
organization security settings, rulesets, and per-repository `.github/dependabot.yml`
files. A Dependabot file in this `.github` repository does not become an
organization-wide default for every repository.
