# Threat model

## Assets

Vault funds, authorization privacy, signer-set integrity, payload integrity, nullifier uniqueness, access-package confidentiality, and chat content.

## Adversaries

Malicious callers, compromised clients, curious or malicious relayers/RPCs/transports, database readers, replay attackers, unauthorized members, and compromised operator or upgrade keys.

## Security properties

- Fund movement requires program authorization and exact payload binding.
- Nullifiers prevent repeated authorized actions.
- Wallet-scoped metadata never substitutes for proof.
- Verifier errors fail closed.
- Fee and reimbursement arithmetic is bounded and checked.

## Known limitations

Upgradeable programs introduce governance trust. Relayers, RPCs, browsers, databases, Waku/Logos, and Arcium can observe different metadata. Current devnet roles may share signers. Factory binding for ZK fee-receipt consumption remains under review.
