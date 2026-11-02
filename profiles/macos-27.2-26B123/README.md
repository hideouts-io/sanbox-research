# macOS 27.2 (26B123)

Snapshot ID: `macos-27.2-26B123`. Declared version: `27.2`; declared build: `26B123`.

This snapshot contains **611 recorded `.sb` paths** and **2,833,018 bytes**. Attribution: **declared-unverified**. Coverage: **recorded-paths-only**.

Source: Local capture; no source URL recorded.

Source revision: `unavailable`.

The original installed-relative paths are retained below this directory. Original symlink entries are represented by regular files containing the verified target bytes; [the catalog](../../data/catalog.json) retains their original link declarations.

Verify the profile files from this snapshot directory:

```sh
shasum -a 256 -c SHA256SUMS
```

[Snapshot provenance](provenance.json) | [Complete provenance](../../data/provenance.json) | [Collection overview](../../README.md)

## Qualifications

- Product version 27.2, build 26B123 and arm64 were observed locally with sw_vers and uname during acquisition; no independent immutable Apple host attestation was obtained.
- Only .sb paths under the two standard profile roots were recorded. Other sandbox policy locations, compiled policies and effective process policies are outside this capture.
- Source path set, dereferenced byte hashes, sizes and symbolic-link targets matched independent inventories before and after copying; this is a point-in-time consistency check, not atomic acquisition or proof of authenticity.
- Release channel is unknown; no stable or beta declaration is inferred from the version or build string.
- Acquisition time is the local UTC clock observation, not independent timestamp attestation. Private host inventories and acquisition reports remain outside the public collection.
- Saved-byte consistency and derived textual markers do not establish Apple authenticity, safety, loaded policy, effective authorization or runtime behavior.

No policy was compiled, applied, or executed for publication. Hashes establish byte consistency with the saved catalog, not Apple authenticity, actual loading, effective authorization, or process behavior.
