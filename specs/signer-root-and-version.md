# Signer root and version

The signer commitment root commits to the authorized signer set without storing a public member list. The signer-set version monotonically identifies the active set.

Authorization must match both the current vault root/version and the proposal snapshot. A signer-set change supplies current and next values, validates the canonical change payload, and increments the version. Wallet-scoped access records and signer packages are convenience and delivery mechanisms; neither grants authority unless the on-chain root/version accepts the resulting proof.
