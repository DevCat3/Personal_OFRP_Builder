# Personal OFRP Builder

One GitHub Actions workflow (`.github/workflows/ofrp.yml`) that builds OrangeFox Recovery for
**9.0, 10.0, 11.0, 12.1 and 14.1** branches.

Run it from **Actions → OrangeFox Recovery Builder → Run workflow**.

| Branch | Makefile | Java | Python | Build command |
|---|---|---|---|---|
| 14.1 / 12.1 / 11.0 | `twrp_<device>.mk` | 11 | 3 | `mka adbd <target>image` |
| 10.0 / 9.0 | `omni_<device>.mk` | 8 | 2 | `mka <target>image` |

The makefile is auto-detected (twrp_ / omni_ / fox_), preferring the one that matches the branch.
Use a device tree branch that matches the chosen OrangeFox branch (e.g. `fox_9.0`).
Optional: add `tools/libneeds` and `tools/ldcheck` to the repo to enable the dependency check.
