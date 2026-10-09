# FreeDOS-88VA

A port of [FreeDOS](https://www.freedos.org/) to the NEC PC-88VA. The goal is a FreeDOS 1.4 based system that boots from a 2HD floppy on the PC-88VA, built reproducibly from public sources.

## News

- 2026-10-09: The owner booted FreeDOS M20.1 and the MS-DOS 2.0 and 4.0 preview 2 disks from drive A: on a real PC-88VA2 with 640 KB and ran DIR and CHKDSK; disk access is noticeably faster than with the previous versions (not measured). Other hardware checks are NOT RUN.
- 2026-10-09: Released FreeDOS for the PC-88VA M20.1: the floppy disk code (loader, kernel and disk driver) transfers a whole track per ROM call instead of one sector at a time, cutting floppy commands several-fold on the VAEG emulator (reads 356 to 98, writes 131 to 45 for the same commands). Validated on the VAEG emulator.
  - https://github.com/FreeDOS-88VA/freedos/releases/tag/m20.1
- 2026-10-08: Preview 2 of the PC-88VA MS-DOS 2.0 and 4.0 disks: the disk driver now reads and writes a whole track per ROM call instead of one sector at a time, and uses the drive-door status for media checks, which cuts floppy commands several-fold (validated on the VAEG emulator).
  - MS-DOS 4.0: https://github.com/FreeDOS-88VA/MS-DOS/releases/tag/msdos4-va.2
  - MS-DOS 2.0: https://github.com/FreeDOS-88VA/MS-DOS/releases/tag/msdos2-va.2
- 2026-10-08: Released English MS-DOS 2.0 and 4.0 disks for the PC-88VA from the MIT-licensed Microsoft MS-DOS release (prereleases, validated on the VAEG emulator; the owner booted both from drive A: on a real PC-88VA2 with 640 KiB and ran DIR and CHKDSK, other hardware checks NOT RUN). MS-DOS 4.0 is built from source except two prebuilt libraries that have no source in the release; MS-DOS 2.0 uses the release's MSDOS.SYS, COMMAND.COM and utilities with a PC-88VA IO.SYS built from source. Build recipes: [experiments/msdos4-va](https://github.com/FreeDOS-88VA/freedos/tree/main/experiments/msdos4-va), [experiments/msdos2-va](https://github.com/FreeDOS-88VA/freedos/tree/main/experiments/msdos2-va).
  - MS-DOS 4.0: https://github.com/FreeDOS-88VA/MS-DOS/releases/tag/msdos4-va.1
  - MS-DOS 2.0: https://github.com/FreeDOS-88VA/MS-DOS/releases/tag/msdos2-va.1

## Latest: M20.1

**[M20.1](https://github.com/FreeDOS-88VA/freedos/releases/tag/m20.1)** (VAEG validation; owner booted it on a PC-88VA2 and ran DIR and CHKDSK; faster floppy access than [M20](https://github.com/FreeDOS-88VA/freedos/releases/tag/m20)) is built on the FreeDOS 1.4 release sources (kernel `ke2043`, FreeCOM `com086`). It provides three PC-88VA 2HD floppy images (English only): a bootable system disk, a utilities disk and an archiver/tools disk (UNZIP, ZIP, GZIP, DEBUG). Japanese support is planned for the next milestone.

## Start here

- **[freedos](https://github.com/FreeDOS-88VA/freedos)**: build recipes, pinned sources, documentation, milestone reports and release disk images.
- [M20.1 release notes](https://github.com/FreeDOS-88VA/freedos/blob/main/docs/releases/m20.md), including known issues and the rebuild procedure.
- Earlier releases: [M19 MS-DOS 4 COMMAND preview](https://github.com/FreeDOS-88VA/freedos/releases/tag/m19-msdos4-preview.1) and [M18](https://github.com/FreeDOS-88VA/freedos/releases/tag/m18).

## Repositories

| Area | Repositories |
|---|---|
| Kernel and shell | [kernel](https://github.com/FreeDOS-88VA/kernel) (fork of FDOS/kernel; the older [fdkernel](https://github.com/FreeDOS-88VA/fdkernel) is a lpproj fork kept for M18-M19 history), [freecom](https://github.com/FreeDOS-88VA/freecom) (fork of FDOS/freecom; the older [freecom_dbcs2](https://github.com/FreeDOS-88VA/freecom_dbcs2) is a lpproj fork kept for M18-M19 history) |
| Assembler | [JWasm](https://github.com/FreeDOS-88VA/JWasm) |
| Utility forks (Open Watcom / PC-88VA changes) | [choice](https://github.com/FreeDOS-88VA/choice), [deltree](https://github.com/FreeDOS-88VA/deltree), [comp](https://github.com/FreeDOS-88VA/comp), [fc](https://github.com/FreeDOS-88VA/fc), [attrib](https://github.com/FreeDOS-88VA/attrib), [tree](https://github.com/FreeDOS-88VA/tree), [DOS-debug](https://github.com/FreeDOS-88VA/DOS-debug) |
| FreeDOS 1.4 package imports | [replace](https://github.com/FreeDOS-88VA/replace), [exe2bin](https://github.com/FreeDOS-88VA/exe2bin), [swsubst](https://github.com/FreeDOS-88VA/swsubst), [undelete](https://github.com/FreeDOS-88VA/undelete), [unzip](https://github.com/FreeDOS-88VA/unzip), [zip](https://github.com/FreeDOS-88VA/zip), [gzip](https://github.com/FreeDOS-88VA/gzip) |
| MS-DOS | [MS-DOS](https://github.com/FreeDOS-88VA/MS-DOS) (fork of Microsoft's source release: MS-DOS 4 COMMAND.COM for the FreeDOS disk, and the PC-88VA MS-DOS 2.0/4.0 disks on branch `release/msdos-va`) |

Component source stays in these repositories; `freedos` pins exact commits. Each import's `PROVENANCE.md` records its upstream package and hashes.
