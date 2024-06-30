# Smart-Contract-Management-Project-Function-Frontend

The Assessment contract is designed to manage deposits and withdrawals for an account. It ensures that only the owner of the contract can perform these actions. The contract includes mechanisms to handle deposits and withdrawals, track the balance, and emit events when transactions occur.

State Variables
owner: An address variable that holds the owner's address. The owner is the one who deployed the contract.
balance: A uint256 variable that holds the current balance of the account.
Events
Deposit: Emitted when a deposit is made, with the amount deposited.
Withdraw: Emitted when a withdrawal is made, with the amount withdrawn.
Constructor
The constructor is executed once when the contract is deployed. It initializes the contract's owner and starting balance.
Parameters:
initBalance: Initial balance to be set for the contract.
Functions
getBalance

Description: Returns the current balance of the account.
Visibility: public view
Returns: uint256 - The current balance.
deposit

Description: Allows the owner to deposit a specified amount into the account.
Visibility: public payable
Parameters:
_amount: The amount to be deposited.
Requirements: The sender must be the owner.
Effects: Increases the balance by the deposited amount.
Events: Emits a Deposit event with the deposited amount.
withdraw

Description: Allows the owner to withdraw a specified amount from the account.
Visibility: public
Parameters:
_withdrawAmount: The amount to be withdrawn.
Requirements: The sender must be the owner. The balance must be sufficient for the withdrawal.
Effects: Decreases the balance by the withdrawn amount.
Events: Emits a Withdraw event with the withdrawn amount.
Custom Error: InsufficientBalance - Thrown if the balance is insufficient for the withdrawal.
