# Fees and reimbursement

- Vault creation requires a funded ZK Pool fee receipt before factory creation.
- A receipt is one-time and bound to an intent hash.
- The current ZK Pool consume instruction validates the receipt and intent but does not independently bind its signer named `factory` to the Private Vault config factory. This boundary is under review.
- Proposals pin a maximum reimbursement and reimbursement wallet.
- Execution supplies actual reimbursement and must not exceed the proposal cap.
- Protected withdrawals may pin a minimum recipient amount.
- Program-owned accounts preserve required Solana rent. Additional operational reserve policy must not be confused with on-chain rent enforcement.
