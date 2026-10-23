# Release Manifest Contract

Status: schema proposal; no public release artifacts currently exist.

A release manifest should bind:
- Release channel and version.
- Source commit and profile revision.
- Builder/toolchain versions and resolved upstream snapshots.
- ISO artifact name, byte size and SHA-256 digest.
- SBOM and build provenance references.
- VM boot-test result and logs.
- License/attribution summary.
- Known limitations, supported target and recovery instructions.
- Signature metadata and key identity, once the trust system is implemented.

Promotion rules:
1. Reject missing or mutable source references.
2. Reject absent artifacts, digest mismatches, failed VM acceptance tests or missing provenance.
3. Keep signing and publication credentials outside the build job.
4. Publish prototypes under an explicit experimental label.
5. Never call a build stable or production-ready based solely on successful compilation or a single VM boot.
