# IPCONFIG.R4X

`IPCONFIG.R4X` is an independent R4OS application implemented in Zig.

## Package

- Package version `0.1.5`
- Image target: `/R4OS/SOFTWARE/TERMINAL/IPCONFIG.R4X`
- Image scope: `full`
- Canonical project manifest: `module.R4MF`

The manifest is the single source of truth for the artifact, imports, image
target, and package metadata.

## Build

On Windows:

    Build.bat

On Linux

    ./Build.sh

The build starters resolve the current local R4OS dependency checkouts through
`Settings.R4S`. The URL and hash entries in `build.zig.zon` record the
last verified standalone dependency identities; workspace builds use the
mapped local checkouts.

## Documentation

Detailed German technical notes from the migration are preserved in
`DOCUMENTATION.de.txt`. Source-transfer provenance is recorded in
`PROVENANCE.txt`.

## License

Original R4OS material is licensed under Apache License 2.0. See `LICENSE`
and `NOTICE`. Any repository-specific external material is documented in
`THIRD_PARTY_NOTICES.md`.

## API migration 0.90.69

The normal build selects SDK202, App2, R4XStart2 and platform Query2.
The exact dependencies and ordered imports belong to module.R4MF.

The existing /ALL, /RENEW, /RELEASE and dash aliases retain their purpose.
The whole argument is parsed by ArgCursor. DHCP action and status share one
checked budget. Actual protocol/service Info calls report IPv6 interfaces,
provider and link generations, addresses, routes and capabilities. A changing
inventory is marked for refresh. Missing providers retain unknown data.
