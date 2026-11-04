# manifests — RMX1992 (Realme X2) local manifests

> **Note:** All documentation and code in this project are purely AI-generated.

Local manifests for building **LineageOS 24.0 (Android 17)** for Realme X2
(RMX1991/1992/1993) on **ServerHive** (Bot 8 node, rental to 2026-11-12 02:43 IST;
the 23.2-era builds ran on crave.io, LOS 23.2 project ID 99).

> **ACTIVE BUILD LINE: `lineage-24.0`** — declared in
> [`../../BUILD_TARGET`](../../BUILD_TARGET). The build clones **this repo's `lineage-24.0`
> branch** (`git clone ... -b lineage-24.0`) into `.repo/local_manifests/` after
> `repo init -b lineage-24.0`. The filename used is `rmx1992_lineage_24.xml`.

**Branch `lineage-24.0`** layer-repo pins (all public, all on branch `lineage-24.0`):
- `octal-illumination/android_device_realme_X2` — proven A16 adaptation chain (129 commits)
  carried linearly onto the 24.0 line (decision D1,
  `roms/docs/2026-11-05-los24-line-switch-plan.md`)
- `octal-illumination/android_kernel_realme_sm6150` — RjTangpos 4.14.357-openela base + our
  Kconfig-hygiene commit (`9f1b190c`, decision D2)
- `octal-illumination/android_vendor_realme_X2` — F.26 OFP harvest (phase-2b final state) +
  the ELF/Soong fix chain

Workspace governance: `~/Projects/android/devices/rmx1992/roms/CRAVE-COMPLIANCE.md`
(ban rules R1–R12, mechanically enforced by crave-guard.sh). ServerHive ops rules:
`roms/docs/2026-11-04-serverhive-build-ops-notes.md`.

---

## Versions table (one-handle-per-version map)

| Version line | Manifests branch | device @ | kernel @ | vendor @ | Status |
|---|---|---|---|---|---|
| **LOS 24.0 (A17)** — the active line | `lineage-24.0` | `lineage-24.0` | `lineage-24.0` | `lineage-24.0` | ACTIVE — all A17 adaptation commits land here |
| **LOS 23.2 (A16)** — proven green (20261102 zip, hash-verified on Passport) | `lineage-23.2` | `lineage-23.2` | `lineage-23.2` | `lineage-23.2` | PARKED — artifact set archived; revive only on user request |

Conventions: fix commits carry `X2-Fix: version-neutral` or `X2-Fix: a17-specific` footers; cross-line propagation is manual cherry-pick (never auto-merge). Future flavors: one manifests branch per flavor (`<flavor>-<version>`), forked from the newest known-good line, only after a version builds + boots.
