# 13.52 source update

Updated from Scene-Collective/ps4-hen commit `2beb4cf` (Add 13.52 support).

Imported into `ps4_offsets.js`:
- verified 13.52 kernel offsets already present in this tree were retained.
- added the 13.52 kernel patch-site table from `installer/include/offsets.h`.
- recorded pmap, copyin/copyout/copyinstr, setlogin, PFS, debug-RIF, debug-settings and depth-limit sites.

Intentionally not changed:
- `kpatch` remains `null`; the local `chain_poops.js` expects a binary patch format that is not established by the upstream source.
- WebKit offsets remain `NEEDS-DUMP`; no unverified WebKit gadgets were invented.

Upstream also raises `MAX_FW` to 1352 and adds a dedicated `1352.c` payload-offset table.

Sources:
- https://github.com/Scene-Collective/ps4-hen/commit/2beb4cf
- https://github.com/ps4-linux/ps4-linux-loader/releases/tag/v25
