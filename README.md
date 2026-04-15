# tgr_codegen

Public distribution repository for the formal release flow of
`JiepengTan/tg_codegen`.

This repository does not store source code. It stores mirrored GitHub Release
assets from the source repository, validates the release manifest plus bundle
checksums.

Current expected assets per tag:

- `codegen-linux-amd64.zip`
- `codegen-linux-arm64.zip`
- `codegen-osx-amd64.zip`
- `codegen-osx-arm64.zip`
- `codegen-win-amd64.zip`
- `codegen-win-arm64.zip`
- `manifest.json`
- `SHA256SUMS.txt`

Current manifest contract for `codegen` releases:

- `mode` is `release`
- `component` is `codegen`
- each `bundles[]` entry uses `name=codegen-{os}-{arch}.zip`
- each `bundles[]` entry uses `os=linux|osx|win`
- each `bundles[]` entry uses `arch=amd64|arm64`
- each `bundles[]` entry carries `name`, `os`, `arch`, and a
  `bundle-entry-exists` validation with required bundle paths
