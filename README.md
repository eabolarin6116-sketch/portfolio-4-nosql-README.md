# Portfolio 4: NoSQL and Advanced Data Models

## 1. Case Study

The Bank/Fintech Platform manages customers, accounts, transfers, deposits, withdrawals, and transaction audit logs.

## 2. Objective

This portfolio explores how a document-oriented NoSQL database can represent and retrieve financial transaction information.

## 3. Proposed NoSQL Database

MongoDB is selected as the proposed document database. It stores records as BSON documents and supports flexible document structures.

## 4. Proposed Data Model

A `customers` collection will store customer profile information. A `transactions` collection will store transaction details, including the account identifier, transaction type, amount, status, timestamp, and relevant transfer details.

## 5. Suitability

A document database can be useful for transaction-history views, audit-event records, and application data with varying structures. However, financial balances and transfers still require appropriate consistency controls and careful transaction design.

## 6. Implementation Evidence

Screenshots of the database setup, sample documents, and query results will be added after implementation.

## 7. Conclusion

This portfolio will demonstrate a document-oriented model for the Bank/Fintech Platform and evaluate its suitability alongside the existing PostgreSQL relational database.

## 8. Documentation

The following documents describe the NoSQL implementation and its suitability:

- [`nosql-data-model.md`](nosql-data-model.md) — MongoDB collection structure, document fields, and query results.
- [`suitability-analysis.md`](suitability-analysis.md) — benefits, limitations, and comparison with PostgreSQL.

## 9. Implementation Evidence

The following screenshots document the implementation:

| Evidence | What it demonstrates |
|---|---|
| MongoDB cluster dashboard | The hosted MongoDB environment is available |
| Database and collection | The `bank_fintech` database and `transactions` collection exist |
| Inserted documents | Three sample transaction documents were inserted |
| Successful-transactions query | Filtering by successful status returns three documents |
| Deposit query | Filtering by deposit type returns one document |

Screenshots should be stored in an `evidence/` subfolder. Replace the descriptions with links to the actual screenshots after adding them to GitHub.

## 10. Assessment Summary

This portfolio demonstrates:

1. A document-oriented NoSQL data model for the Bank/Fintech case study.
2. A working MongoDB collection containing sample transaction documents.
3. Queries that retrieve transactions by status and type.
4. An evaluation of MongoDB's suitability, limitations, and relationship to the existing PostgreSQL implementation.

## 11. Conclusion

The MongoDB exercise demonstrates an alternative way to represent and query transaction information. PostgreSQL remains the primary relational implementation for the demonstrated account and transfer operations, while MongoDB illustrates the flexibility of a document-oriented model. The sample implementation is educational and is not a production banking system.
