# Proposal lifecycle

1. The relayer creates a proposal containing a canonical payload hash and snapshots of threshold, member count, signer root, and signer-set version.
2. An authorized signer obtains an Arcium-backed receipt bound to the proposal and an action-specific nullifier.
3. The program verifies receipt ownership, status, root, version, action domain, nullifier, payload hash, and freshness fields.
4. Approve or reject records consume a unique nullifier and update public counts.
5. Threshold or rejection rules transition proposal status.
6. Execution recomputes and checks the canonical payload, fee protections, balances, and rent requirements before moving funds or changing state.

Deterministic validation must fail before simulation when practical. Metadata is never authorization.
