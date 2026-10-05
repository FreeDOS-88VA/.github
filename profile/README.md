# FreeDOS-88VA

A port of [FreeDOS](https://www.freedos.org/) to the NEC PC-88VA. The goal is a FreeDOS 1.4 based system that boots from a 2HD floppy on the PC-88VA, built reproducibly from public sources.

## Latest: M20 release candidate 1

**[M20 release candidate 1](https://github.com/FreeDOS-88VA/freedos/releases/tag/m20-rc.1)** (prerelease, emulator validation only; hardware NOT RUN) is built on the FreeDOS 1.4 release sources (kernel `ke2043`, FreeCOM `com086`). It provides three PC-88VA 2HD floppy images (English only): a bootable system disk, a utilities disk and an archiver/tools disk (UNZIP, ZIP, GZIP, DEBUG). Japanese support is planned for the next milestone.

## Start here

- **[freedos](https://github.com/FreeDOS-88VA/freedos)**: build recipes, pinned sources, documentation, milestone reports and release disk images.
- [M20 release notes](https://github.com/FreeDOS-88VA/freedos/blob/main/docs/releases/m20.md), including known issues and the rebuild procedure.
- Earlier releases: [M19 MS-DOS 4 COMMAND preview](https://github.com/FreeDOS-88VA/freedos/releases/tag/m19-msdos4-preview.1) and [M18](https://github.com/FreeDOS-88VA/freedos/releases/tag/m18).

## Repositories

| Area | Repositories |
|---|---|
| Kernel and shell | [kernel](https://github.com/FreeDOS-88VA/kernel) (fork of FDOS/kernel; the older [fdkernel](https://github.com/FreeDOS-88VA/fdkernel) is a lpproj fork kept for M18-M19 history), [freecom](https://github.com/FreeDOS-88VA/freecom) (fork of FDOS/freecom; the older [freecom_dbcs2](https://github.com/FreeDOS-88VA/freecom_dbcs2) is a lpproj fork kept for M18-M19 history) |
| Assembler | [JWasm](https://github.com/FreeDOS-88VA/JWasm) |
| Utility forks (Open Watcom / PC-88VA changes) | [choice](https://github.com/FreeDOS-88VA/choice), [deltree](https://github.com/FreeDOS-88VA/deltree), [comp](https://github.com/FreeDOS-88VA/comp), [fc](https://github.com/FreeDOS-88VA/fc), [attrib](https://github.com/FreeDOS-88VA/attrib), [tree](https://github.com/FreeDOS-88VA/tree), [DOS-debug](https://github.com/FreeDOS-88VA/DOS-debug) |
| FreeDOS 1.4 package imports | [replace](https://github.com/FreeDOS-88VA/replace), [exe2bin](https://github.com/FreeDOS-88VA/exe2bin), [swsubst](https://github.com/FreeDOS-88VA/swsubst), [undelete](https://github.com/FreeDOS-88VA/undelete), [unzip](https://github.com/FreeDOS-88VA/unzip), [zip](https://github.com/FreeDOS-88VA/zip), [gzip](https://github.com/FreeDOS-88VA/gzip) |
| MS-DOS reference | [MS-DOS](https://github.com/FreeDOS-88VA/MS-DOS) (fork of Microsoft's source release) |

Component source stays in these repositories; `freedos` pins exact commits. Each import's `PROVENANCE.md` records its upstream package and hashes.
