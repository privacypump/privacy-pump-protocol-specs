# Authority roles

| Role                   | Responsibility                                         | Required separation                                   |
| ---------------------- | ------------------------------------------------------ | ----------------------------------------------------- |
| Config authority       | Initializes the shared program configuration           | Must be governed as a high-trust role                 |
| Factory                | Creates vault accounts after fee verification          | Distinct protocol role from relayer                   |
| Relayer                | Submits authorized proposal and execution transactions | Must not bypass payload or receipt checks             |
| Vault treasury         | Program-derived account holding vault funds            | Not an operator wallet                                |
| Reimbursement wallet   | Receives bounded relayer reimbursement                 | Pinned in proposal data                               |
| Keeper                 | Triggers eligible fee settlement                       | Cannot select an arbitrary destination                |
| Settlement destination | Receives settled creation fees                         | Stored in settlement state                            |
| Upgrade authority      | Can replace upgradeable program code                   | Shared devnet authority is a central trust assumption |

Factory and relayer are distinct roles, but a deployment may assign one signer to both. Production signer topology is intentionally not published.
