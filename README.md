# nanlm-ram — NaNLMind sparse mutable RAM tier

Managed by `NaNLMind/.github/workflows/nanlm-bootstrap.yml` using deeprepo's
`deepcore` sparse tier engine. Do not clone for data; readers use HTTP Range.

- 16 release bins × 510 pages × 4 MiB = 31.9 GiB sparse virtual
- per-page 4 MiB, append-only delta journal + compaction
- stores `nanlm/` head packets, clock, lease, manifest, round records
- separate from Qwen's `reporam`, so both rings can run without sharing a writer
