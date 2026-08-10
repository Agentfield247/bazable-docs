# bazable accept

Accepts a pending AI‑generated proposal and applies the schema changes to the contract.

## Usage
```bash
bazable accept <proposalId>

Options
None.

Prerequisites
At least one pending proposal must exist in the contract. Proposals are created with bazable propose.

The proposal ID is shown when the proposal is created, or you can view all pending proposals with bazable config --get pending_proposals.

What it does
Finds the proposal with the given ID in the pending_proposals array.

Merges the proposed request and response schema changes into the corresponding endpoint.

Marks the proposal as accepted with a timestamp.

After acceptance, the updated contract can be pushed to the cloud (bazable push) so the whole team stays in sync.

## Example
bazable propose "Add a phone_number field to the POST /v1/users endpoint"
# Proposal ID: 1691501234567

bazable accept 1691501234567
# Proposal accepted and applied. Updated endpoint: POST https://api.example.com/v1/users
