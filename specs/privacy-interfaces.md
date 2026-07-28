# Privacy interfaces

## Arcium receipt interface

A verified receipt binds request, vault, proposal, signer root, signer-set version, action domain, nullifier, payload hash, computation identity, slot, and consumption state. The consuming program verifies the account owner and complete binding and fails closed.

## ZK Pool research interface

Notes commit to private transfer state. Roots establish membership, nullifiers prevent repeat spends, and public inputs bind amount, pool, destination, and route domain. The verifier integration is fail-closed by default and is not a complete production privacy system.

## Access-package concept

Packages are wallet-scoped and vault-scoped encrypted delivery objects. They carry no authority by themselves. The active on-chain root and version remain authoritative.

## Waku and Logos communication concept

Message content and room keys should be encrypted end to end. Transport topics, timing, peers, browser storage, membership coordination, and infrastructure can still leak metadata. Chat access follows the same vault access gate.
