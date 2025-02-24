Assignment : Banking System
Scenario
You are a database administrator for a banking system. The bank wants to optimize
performance using indexes, implement functions for business logic, create stored
procedures for common operations, and use triggers to maintain data integrity.
Task 1: Implement Indexing for Performance Optimization
Requirement
1. 2. 3. 4. Create a clustered index on the AccountID column in the Accounts table.
Create a non-clustered index on the CustomerName column in the Customers table
for faster searching.
Create a composite index on the TransactionDate and Amount columns in the
Transactions table.
Create a unique index on the AccountNumber column in the Accounts table to
prevent duplicate accounts.
Task 2: Create a Scalar Function for Interest Calculation
Requirement
1. 2. 3. Create a scalar function that calculates the interest for a given AccountID.
The function should take AccountID as input and return the calculated interest based
on an annual interest rate of 5%.
Use this function in a SELECT query to display the interest for each account.
Task 3: Create a Stored Procedure for Transactions
Requirement
1. Create a stored procedure to transfer money between two accounts.
2. The procedure should:
o Accept FromAccountID, ToAccountID, and Amount as parameters.
o Check if the FromAccountID has sufficient balance before transferring.
o Deduct the amount from FromAccountID and add it to ToAccountID.
o Insert a record into the Transactions table with details of the transfer.
3. Execute the stored procedure for testing.
Task 4: Implement a Trigger for Preventing Overdrafts
Requirement
1. Create a trigger that prevents withdrawals if the balance is insufficient.
2. The trigger should:
o Fire before an update on the Accounts table when a withdrawal transaction
occurs.
o Prevent the transaction if the account balance goes below zero.
o Display a message "Insufficient funds! Transaction aborted."
3. Test the trigger by trying to withdraw an amount greater than the account balance.
Task 5: Implement an Audit Trigger for Transactions
Requirement
1. 2. 3. Create an AFTER INSERT trigger on the Transactions table.
The trigger should log every transaction (AccountID, Amount, Date) into an
Audit_Transactions table.
Insert some sample transactions and verify that the audit table captures all changes.
Expected Tables for Testing
• Customers(CustomerID, CustomerName, Email, PhoneNumber)
• Accounts(AccountID, CustomerID, AccountNumber, Balance, AccountType)
• Transactions(TransactionID, AccountID, TransactionType, Amount,
TransactionDate)
• Audit_Transactions(AuditID, AccountID, Amount, TransactionDate,