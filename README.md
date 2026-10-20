# manifests — RMX1992 (Realme X2) local manifests

> **Note:** All documentation and code in this project are purely AI-generated.

Local manifests for building **LineageOS 24.0 (Android 17)** for Realme X2
(RMX1991/1992/1993) on **crave.io** (foss instance, LOS 23.2 project ID 99 +
repo-init re-target — user-locked build path, 2026-10-15).

**Branch `lineage-24.0`** is wired into builds by cloning this repo into
`.repo/local_manifests/` (see the gate-verified build command in
`roms/CRAVE-PIPELINE.md` §5.2 of the workspace).

Layer repos (all public, all on branch `lineage-24.0`):
- `octal-illumination/android_device_realme_X2` (fork of RjTangpos @A16 — A16→24.0 adaptation pending)
- `octal-illumination/android_kernel_realme_sm6150` (RjTangpos 4.14.357 base — rebase onto LineageOS sm6150 lineage-24.0 pending)
- `octal-illumination/android_vendor_realme_X2` (F.26 OFP extraction + sm6150-common donors — placeholder — extraction pending (Phase-2b, user hold))

Workspace governance: `~/Projects/android/devices/rmx1992/roms/CRAVE-COMPLIANCE.md`
(ban rules R1–R12, mechanically enforced by crave-guard.sh).

---

## Versions table (one-handle-per-version map)

| Version line | Manifests branch | device @ | kernel @ | vendor @ | Status |
|---|---|---|---|---|---|
| **LOS 23.2 (A16)** — the working line | `lineage-23.2` | `lineage-23.2` | `lineage-23.2` | `lineage-23.2` | ACTIVE (job 306550 era) — all build fixes land here |
| **LOS 24.0 (A17)** — adaptation line | `lineage-24.0` | `lineage-24.0` | `lineage-24.0` | `lineage-24.0` | FROZEN until the A16 line builds+boots; then A17 adaptation commits land on these branches |

Conventions: fix commits carry `X2-Fix: version-neutral` or `X2-Fix: a16-specific` footers; cross-line propagation is manual cherry-pick (never auto-merge). Future flavors: one manifests branch per flavor (`<flavor>-<version>`), forked from the newest known-good line, only after a version builds + boots.
