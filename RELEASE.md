# Release

- [ ] Update version in `Cargo.toml`.
- [ ] Update `CHANGELOG.md` with version and publication date.
  - To get the changes to the crate since the last release, you can use a
    command like the following:
    ```bash
    git log tes-v0.1.0..HEAD --oneline
    ```
- [ ] Run tests: `cargo test --all-features`.
- [ ] Run linting: `cargo clippy --all-features`.
- [ ] Run fmt: `cargo +nightly fmt --check`.
- [ ] Run doc: `cargo doc`.
- [ ] Stage changes: `git add Cargo.toml CHANGELOG.md`.
- [ ] Create git commit:
  ```
  git commit -m "release: bumps `tes` version to v0.1.0"
  ```
- [ ] Create git tag:
  ```
  git tag tes-v0.1.0
  ```
- [ ] Push release: `git push && git push --tags`.
- [ ] Go to the Releases page in Github, create a Release for this tag, and
      copy the notes from the `CHANGELOG.md` file.
