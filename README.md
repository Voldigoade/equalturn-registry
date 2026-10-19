# Equalturn registry distribution

This repository is the dedicated TUF publication repository for the Equalturn AI ecosystem registry. It was created from the upstream [TUF-on-CI template](https://github.com/theupdateframework/tuf-on-ci-template) and will carry signed TUF metadata and release targets when the publication root ceremony is complete.

## Source of truth

The reviewed registry source remains in [Voldigoade/equalturn](https://github.com/Voldigoade/equalturn), at registry/registry-v3.json. Contributors propose research changes there, where the schema and semantic validator run in CI. A release target is generated deterministically from an approved source revision and then introduced here through the TUF-on-CI signing workflow. Published targets are generated artifacts; they are not edited by hand.

## Current status

The repository layout and publication workflow are initialized from the upstream template. **No Equalturn trusted root, signing keys, TUF metadata, or registry target has been published.** This repository is not yet a usable trusted update source. Do not trust a target from it until a future Equalturn release pins the initial root out of band and the first metadata set is established through the documented threshold signing ceremony.

The GitHub Pages deployment, signing roles, root threshold, online-signing provider, and any credentials remain unconfigured pending that ceremony. Keep those decisions and permissions minimal. Do not commit private keys, signer configuration, credentials, or local signing state.

## Trust boundary

TUF authenticates that a published target was authorized by this repository's trusted metadata and has the expected bytes. It does not establish that an indicator is factually correct, current, safe to block, or evidence that a participant used AI. Registry content remains researched data, not enforcement policy.

See [the Equalturn registry trust design](https://github.com/Voldigoade/equalturn/blob/main/docs/registry-trust.md) for the threat model, roles, rotation, expiry, and release workflow.
