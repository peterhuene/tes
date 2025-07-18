# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased

## 0.8.0 - 06-04-2025

### Changed

- Added `thiserror` dependency for custom error types ([#18](https://github.com/stjude-rust-labs/tes/pull/18)).

## 0.7.0 - 05-20-2025

### Fixed

- Added missing fields on several TES types ([#17](https://github.com/stjude-rust-labs/tes/pull/17)).

### Changed

- Refactored `tes` crate API into request and response representations ([#17](https://github.com/stjude-rust-labs/tes/pull/17)).

## 0.6.0 - 04-30-2025

### Added

- Added missing `State` enum variants ([#11](https://github.com/stjude-rust-labs/tes/pull/11)).
- Added missing `ignore_error` field to `Executor` ([#10](https://github.com/stjude-rust-labs/tes/pull/10)).

## 0.5.0 - 02-21-2025

### Changed

- Updated dependencies to latest to remove dependency on unmaintained crate ([#7](https://github.com/stjude-rust-labs/tes/pull/7)).

## 0.4.1 - 02-21-2025

### Revised

- Removes the `Cargo.lock` so that dependencies may be freely updated.

## 0.4.0 - 02-07-2025

### Revised

- Changes out the `anyhow` error type for `miette`
  ([#5](https://github.com/stjude-rust-labs/tes/pull/5)).
- Removes the `Eq` and `Ord` trait from types containing a `f64` via removal of
  `ordered_float` ([#6](https://github.com/stjude-rust-labs/tes/pull/6)).

## 0.3.0 - 01-30-2025

### Added

- Adds `v1::types::responses::task::View` so it can be accepted as a query
  parameter in downstream crates.

### Revised

- Promotes the `v1::types::responses::service` module to public.
- Gates serialization/deserialization behind the `serde` feature.
- Makes most structs `Clone`.
- Converts `ServiceInfo` to use a builder for construction.
- Changes the `v1::types::responses::service` module to
  `v1::types::responses::service_info`.
- Makes `v1::types::task::State` `Copy`.
- Adds the `ord` feature for all types.

### Fixed

- Removed errant `#[serde(untagged)]` for `v1::types::responses::task::View`.
- Fixes multiple fields that should not be serialized if `None`
  ([#4](https://github.com/stjude-rust-labs/tes/pull/4)).
- Corrects the `outputs` key on a `TaskLog` to be non-optional
  ([#4](https://github.com/stjude-rust-labs/tes/pull/4)).

## 0.2.0 - 08-08-2024

### Added

- Added initial version of the crate.

## 0.1.0

> A note on v0.1.0: this version was accidentally released when reserving the
> `tes` package name on [crates.io](https://crates.io/crates/tes). As such,
> v0.1.0 is technically an empty release: it was yanked from crates.io, and
> v0.2.0 is the first _real_ version of the crate.
