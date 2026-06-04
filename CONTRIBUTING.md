# Contributing to StudioDrave

Thank you for contributing. This guide applies to all StudioDrave repositories.

## Branching

All repositories follow the same branching model:

```
feature/* → develop → main
```

- Cut feature branches from `develop`
- Open PRs into `develop`
- `develop` → `main` triggers the release pipeline
- Never commit directly to `main` or `develop`

## Commit messages

All commits must follow [Conventional Commits](https://www.conventionalcommits.org):

```
type: short description

Types: feat, fix, docs, chore, refactor, test, style, perf, ci
```

Examples:
```
feat: add StatCard component
fix: correct AppHeader touch target to 44pt
docs: update navigation integration guide
chore: upgrade Kotlin to 2.0
```

Breaking changes:
```
feat!: redesign theming contract

BREAKING CHANGE: DraveTheme now requires a seedColor parameter
```

Commit messages are validated automatically on every PR via our
[conventional commits workflow](.github/workflows/conventional-commits.yml).

## Pull requests

- One logical change per PR
- PRs that touch both Android and iOS must include both platform implementations
- All PRs require at least one reviewer
- Squash merge into `develop`

## Code style

- **Kotlin/Compose**: follow [Compose API guidelines](https://android.googlesource.com/platform/frameworks/support/+/androidx-main/compose/docs/compose-api-guidelines.md)
- **Swift/SwiftUI**: follow [Swift API Design Guidelines](https://www.swift.org/documentation/api-design-guidelines/)
- No hardcoded colors, sizes, or strings — always use DraveUI tokens and string resources

## Questions

Open a GitHub Discussion or reach out to the team directly.
