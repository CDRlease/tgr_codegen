# tgr_codegen

Public distribution repository for the formal release flow of
`JiepengTan/tg_codegen`.

This repository does not store source code. It stores mirrored GitHub Release
assets from the source repository, validates the release manifest plus bundle
checksums, and then notifies
`JiepengTan/tg_client`.

Current expected assets per tag:

- `codegen-generator-<rid>.zip`
- `manifest.json`
- `SHA256SUMS.txt`

Current manifest contract for `codegen` releases:

- `mode` is `release`
- `component` is `codegen`
- each `bundles[]` entry carries `name`, `os`, `arch`, and a
  `bundle-entry-exists` validation with required bundle paths

Required secret:

- `CLIENT_DISPATCH_TOKEN`: token used to send `repository_dispatch` events to
  `JiepengTan/tg_client`
