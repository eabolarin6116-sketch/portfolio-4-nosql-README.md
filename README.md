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
