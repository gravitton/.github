# Contributing

Thanks for taking the time. These libraries are small and opinionated, so a short conversation
first saves work on both sides.

## Before you start

- **Bug fixes** are welcome as a pull request straight away. Include a test that fails without
  the fix.
- **New API or a change to existing API**: open an issue first and describe the use case. A
  method is added when a caller needs it, not for symmetry with another type or library.
- **Breaking changes** are marked **breaking** in the changelog, whose header states the
  release policy of the module. There are no major version bumps and no deprecated aliases.

## Code

- Follow the code around your change: the order of methods in a file, the naming, the form of
  doc comments. A new method goes where its siblings are.
- Every exported identifier has a doc comment that says what it returns, for which inputs, and
  every panic. Describe behaviour in words, without numeric examples.
- Degenerate input returns an answer; a panic is only for an argument with no meaning.

## Tests

- Name tests `Test<Type>_<Method>` or `Test<Function>`, with cases as `t.Run` sections named
  for what they assert.
- Add example cases and a property check (a round-trip, a symmetry, or two methods that must
  agree). Pin allocation counts where the package does.
- Coverage stays at 100%.

## Checks

These must pass, as they do in CI:

```sh
go vet ./...
staticcheck ./...
govulncheck ./...
go test -race -cover ./...
```

Packages with floating-point arithmetic also check in CI that no product is fused into a
multiply-add; wrap a product that feeds a sum in `float64(...)`.

## Changelog

Add your change to the `[Unreleased]` section of `CHANGELOG.md`. Documentation-only changes need
no entry.

By contributing, you agree that your contribution is licensed under the MIT License of the
repository.
