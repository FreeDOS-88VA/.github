# FreeDOS-88VA

A port of [FreeDOS](https://www.freedos.org/) to the NEC PC-88VA. The goal is a FreeDOS 1.4 based system that boots from a 2HD floppy on the PC-88VA, built reproducibly from public sources.

## Start here

- **[freedos](https://github.com/FreeDOS-88VA/freedos)**: build recipes, pinned sources, documentation, milestone reports and release disk images.
- [M18 release](https://github.com/FreeDOS-88VA/freedos/releases/tag/m18) and the [M19 MS-DOS 4 COMMAND preview](https://github.com/FreeDOS-88VA/freedos/releases/tag/m19-msdos4-preview.1).
- Current work: the `m20/freedos-1.4-base` branch (FreeDOS 1.4 kernel `ke2043` and FreeCOM `com086` as the baseline; system, utilities and archiver floppies). Real-hardware testing has not been run.

## Repositories

| Area | Repositories |
|---|---|
| Kernel and shell | [fdkernel](https://github.com/FreeDOS-88VA/fdkernel), [freecom_dbcs2](https://github.com/FreeDOS-88VA/freecom_dbcs2) |
| Assembler | [JWasm](https://github.com/FreeDOS-88VA/JWasm) |
| Utility forks (Open Watcom / PC-88VA changes) | [choice](https://github.com/FreeDOS-88VA/choice), [deltree](https://github.com/FreeDOS-88VA/deltree), [comp](https://github.com/FreeDOS-88VA/comp), [fc](https://github.com/FreeDOS-88VA/fc), [attrib](https://github.com/FreeDOS-88VA/attrib), [tree](https://github.com/FreeDOS-88VA/tree), [DOS-debug](https://github.com/FreeDOS-88VA/DOS-debug) |
| FreeDOS 1.4 package imports | [replace](https://github.com/FreeDOS-88VA/replace), [exe2bin](https://github.com/FreeDOS-88VA/exe2bin), [swsubst](https://github.com/FreeDOS-88VA/swsubst), [undelete](https://github.com/FreeDOS-88VA/undelete), [unzip](https://github.com/FreeDOS-88VA/unzip), [zip](https://github.com/FreeDOS-88VA/zip), [gzip](https://github.com/FreeDOS-88VA/gzip) |
| MS-DOS reference | [MS-DOS](https://github.com/FreeDOS-88VA/MS-DOS) (fork of Microsoft's source release) |

Component source stays in these repositories; `freedos` pins exact commits. Each import's `PROVENANCE.md` records its upstream package and hashes.
