# OctoBay

## Registration

Registration requires an oracle request to check whether the user has created the required repository or not.
This cost can be covered by the registering user or by a pre-existing deposit.

### Payed (Normal)

`register(address _oracle, string memory _githubUser)`

The user sends a transaction (pays gas) and pays the oracle by sending the fee in ETH when calling the `register()` function. The ETH will be converted to LINK to pay the oracle and perform the repository check. If it fails, the user wasted his own funds.

### Prepaid (Gasless)

The user signs a transaction and forwardeds it to a GSN relayer that sends (pays gas for) the transaction. The oracle fee as well as the GSN paymaster expenses are covered by an existing deposit in the OctoBay contract. Required oracle jobs will have an effective fee of 0 LINK but will be payed on fulfillment.

#### User Deposit

#### Issue Deposit
