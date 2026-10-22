# sanbox-research

A public research collection of **23 saved macOS sandbox-profile snapshots**, containing **5,953 recorded `.sb` paths** and **23,561,532 bytes**. This publishes every snapshot currently retained in the SandboxLens reference collection, spanning declared versions 10.9.5 through 27.2 with substantial gaps. It does not cover every macOS release or every policy location.

## Browse the profiles

| Declared macOS version | Declared build | Profiles | Attribution |
| --- | --- | ---: | --- |
| [10.9.5](profiles/macos-10.9.5-13F34/) | `13F34` | 102 | declared-unverified |
| [10.10.5](profiles/macos-10.10.5-14F27/) | `14F27` | 122 | declared-unverified |
| [10.11.6](profiles/macos-10.11.6-15G31/) | `15G31` | 139 | declared-unverified |
| [10.12.6](profiles/macos-10.12.6-16G29/) | `16G29` | 157 | declared-unverified |
| [10.13.6](profiles/macos-10.13.6-17G65/) | `17G65` | 179 | declared-unverified |
| [10.14](profiles/macos-10.14-18A391/) | `18A391` | 190 | declared-unverified |
| [10.14-beta-7](profiles/macos-10.14-beta-7-18A365a/) | `18A365a` | 190 | declared-unverified |
| [10.14-beta-8](profiles/macos-10.14-beta-8-18A371a/) | `18A371a` | 190 | declared-unverified |
| [10.14-beta-9](profiles/macos-10.14-beta-9-18A377a/) | `18A377a` | 190 | declared-unverified |
| [10.14-beta-10](profiles/macos-10.14-beta-10-18A384a/) | `18A384a` | 190 | declared-unverified |
| [10.14.1](profiles/macos-10.14.1-18B75/) | `18B75` | 190 | declared-unverified |
| [10.14.2](profiles/macos-10.14.2-18C54/) | `18C54` | 191 | declared-unverified |
| [10.14.4](profiles/macos-10.14.4-18E226/) | `18E226` | 193 | declared-unverified |
| [10.14.5](profiles/macos-10.14.5-18F132/) | `18F132` | 193 | declared-unverified |
| [10.15](profiles/macos-10.15-19A583/) | `19A583` | 223 | declared-unverified |
| [10.15-beta-1](profiles/macos-10.15-beta-1-19A471t/) | `19A471t` | 217 | declared-unverified |
| [10.15.1](profiles/macos-10.15.1-19B88/) | `19B88` | 223 | declared-unverified |
| [10.15.2](profiles/macos-10.15.2-19C57/) | `19C57` | 223 | declared-unverified |
| [12.6](profiles/macos-12.6-21G115/) | `21G115` | 290 | conflicting |
| [26.6.2](profiles/macos-26.6.2-25G83/) | `25G83` | 570 | declared-unverified |
| [26.7](profiles/macos-26.7-25G229/) | `25G229` | 570 | declared-unverified |
| [27.0](profiles/macos-27.0-26A428/) | `26A428` | 610 | declared-unverified |
| [27.2](profiles/macos-27.2-26B5112a/) | `26B5112a` | 611 | declared-unverified |

Each snapshot preserves the installed-relative path:

```text
profiles/<snapshot-id>/System/Library/Sandbox/Profiles/<name>.sb
profiles/<snapshot-id>/usr/share/sandbox/<name>.sb
```

For example: [27.2 airlock.sb](profiles/macos-27.2-26B5112a/System/Library/Sandbox/Profiles/airlock.sb) and its [snapshot provenance](profiles/macos-27.2-26B5112a/provenance.json).

## Integrity and provenance

- [Catalog](data/catalog.json): per-file SHA-256, byte count, installed-relative path, original symlink declarations, source revision, and narrow textual markers.
- [Provenance](data/provenance.json): source qualifications, acquisition facts where available, coverage limits, and conflicting attribution evidence.
- [SHA256SUMS](SHA256SUMS): checksums of every published file other than the checksum file itself. Each snapshot also contains a profile-only SHA256SUMS file matching its retained saved-tree manifest.

After cloning, verify the complete collection from the repository root:

```sh
shasum -a 256 -c SHA256SUMS
```

All 24 original symlink entries are published as regular `.sb` files containing their verified dereferenced bytes. Original targets remain recorded in the catalog. Profile bytes and embedded notices are preserved without modification.

## Interpretation limits

Version, build, and channel labels are source declarations, not independently authenticated Apple identities. Eighteen snapshots came from pinned community revisions, one from a community report, and four from saved local captures. All snapshots describe recorded paths only.

The Monterey snapshot retains its original `macos-12.6-21G115` identifier, but the source also reports 12.5 / 21G72; its exact profile build remains unresolved. The first three local captures have an unverified `stable` channel declaration; the 27.2 capture records an unknown channel. Big Sur, Ventura, Sonoma, Sequoia, and most intervening point releases are absent.

Static policy text, declared entitlements, loaded policy, and observed runtime behavior are separate evidence. No policy execution or runtime authorization is established by this collection. A textual allow/deny count is not an effective-permission verdict. Private acquisition reports, host inventories, app acceptance logs, and credentials are outside this publication. Profile text retains historical comments and literal paths from its sources.

## Notices

[NOTICE](NOTICE) describes the retained source notices. This collection does not apply SandboxLens's MIT license to Apple or third-party profile text.
