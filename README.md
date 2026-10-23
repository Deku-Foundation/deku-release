# Deku Release Engineering

Release manifests, artifact verification and publication orchestration for Deku Linux.

## Status

Bootstrap stage. There are no supported releases or public ISO artifacts yet.

## Responsibilities

- Define release manifest schema and artifact naming.
- Verify checksums, SBOM, provenance, source commit and CI acceptance evidence before publication.
- Publish release notes and known limitations alongside artifacts.
- Separate untrusted builds from release approval, signing and publication.

## Security

Never commit private signing keys, tokens or credentials. A SHA-256 checksum verifies bytes but does not authenticate who published them. Require signed metadata and a documented key rotation/revocation policy before claiming trusted releases.

## Gate

Do not publish a stable release until the image can be reproduced or its nondeterminism is documented, passes VM boot tests, and has a supported update/recovery policy.
