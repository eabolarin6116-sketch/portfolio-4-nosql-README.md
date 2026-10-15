# NoSQL Data Model — Bank/Fintech Platform

## 1. Selected Database

MongoDB was selected as the document-oriented NoSQL database for the Bank/Fintech Platform. Unlike the PostgreSQL implementation, which stores data in related tables, MongoDB stores records as documents within collections.

## 2. Database and Collection

- **Database:** `bank_fintech`
- **Collection:** `transactions`

The `transactions` collection stores transaction information as individual documents.

## 3. Document Structure

Each transaction document contains the following fields:

| Field | Purpose |
|---|---|
| `_id` | MongoDB-generated unique document identifier |
| `transaction_id` | Application-level transaction reference |
| `account_number` | Account associated with the transaction |
| `transaction_type` | Deposit, withdrawal, or transfer |
| `amount` | Transaction amount |
| `currency` | Currency code, NGN |
| `status` | Transaction processing status |
| `transaction_date` | Date and time of the transaction |
| `destination_account` | Receiving account for a transfer |

The `destination_account` field is present in the transfer example but not in the deposit and withdrawal examples. This illustrates how document structures can vary according to the transaction type.

## 4. Implementation and Query Evidence

Three sample transaction documents were inserted successfully: one deposit, one withdrawal, and one transfer.

Two queries were tested:

1. Filtering by `status: "successful"` returned all three documents.
2. Filtering by `transaction_type: "deposit"` returned one document, `TXN1001`.

Screenshots of the inserted documents and query results provide implementation evidence.

## 5. Comparison with PostgreSQL

PostgreSQL organises the relational model into tables connected by primary and foreign keys. MongoDB stores the transaction records as documents and can accommodate optional fields without requiring every document to have the same structure.

MongoDB's flexibility does not automatically guarantee financial correctness. Account references, transaction identifiers, valid amounts, duplicate prevention, and transfer consistency still require appropriate validation and application logic.

## 6. Conclusion

The MongoDB implementation demonstrates how a document database can represent and retrieve transaction-history information. It complements the PostgreSQL model by illustrating a different data model for the same Bank/Fintech case study. The demonstration uses sample data and does not implement a production banking system.
