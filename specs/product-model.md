# Product model

Privacy Pump has two public products backed by a shared Private Vault program boundary.

## Personal Vault

A Personal Vault is a one-member, threshold-one configuration. It does not have a separate on-chain program in the current architecture.

## Private Multisig

A Private Multisig has multiple authorized members and a threshold. Public state may include threshold, counts, proposal status, and execution status. Creator, member, approver, and rejecter wallet identities must not be exposed by current-product public state.

## Shared implementation

The shared program stores a signer commitment root and signer-set version instead of a public member list. Authorization receipts bind the vault, proposal, root, version, action domain, nullifier, and payload hash.
