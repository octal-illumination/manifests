# Build-tree patches (RMX1992)

> **Note:** All documentation and code in this project are purely AI-generated.

Build-tree patches are applied to the synced LOS tree (the base repos are NOT modified).
`~/sync.sh` on the build host applies every `patches/*.patch` after each `repo sync`
(idempotent: `git apply --check` skips already-applied patches).

| Patch | Target | Why |
|---|---|---|
| 0001-reference-ril-header_libs.patch | hardware/ril/reference-ril | upstream omits header_libs ["ril_headers"]; telephony/ril_cdma_sms.h unfound. Device uses qcril; reference-ril never loads at runtime. |

First applied on lineage-23.2 (2026-10-31, recorded ad-hoc on the node); formalized for the
lineage-24.0 line (2026-11-05).
