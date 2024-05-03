# FinTracker

## Overview

FinTracker is a comprehensive web application designed to help users manage their financial transactions effectively. It provides insights into their financial habits, aiding in better financial planning and management. The application is developed using the MERN stack, ensuring a robust and scalable solution for personal finance management.

## Goals

- To develop a user-friendly web interface that allows users to track their income and expenses conveniently.
- To implement secure authentication and data protection features, ensuring the privacy and security of user data.
- To provide financial insights through graphs and summaries, helping users make informed financial decisions.
- (Possibly) To integrate with Lebanese e-wallets to automate data entry and increase accuracy.

## Specifications

### Frontend

- **Dashboard Page**: Features a graphical representation of all transactions and displays total expenses, total balance, and a recent transaction history.
- **Income Page**: Shows total income, lists income entries, and provides functionality to add and delete entries. Possible e-wallet integration to import data.
- **Expense Page**: Manages total expenses and individual expense entries with options to add and delete. Possible e-wallet integration to import data.
- **View Transactions Page**: Offers a consolidated view of all financial transactions, both income and expenses.

### Backend

- **Authentication with JWT (JSON Web Tokens)**: 
  - **Client-Side Storage**: Tokens are stored securely in HttpOnly cookies which are inaccessible via JavaScript to enhance security.
  - **Token Lifecycle Management**: Includes automated expiration and regeneration of tokens upon login to maintain session integrity.
  - **Rate Limiting**: Enforces limits on the number of requests a user can make within a given time frame to prevent abuse.
- **Secure Data Transfer with HTTPS**: Implements HTTPS to ensure all data transmitted between the web server and clients is encrypted, safeguarding against interception.
- **OAuth Integration for Third-Party Authentication**: Enables users to log in using their existing accounts from supported third-party services, streamlining the authentication process and enhancing security.
- **Database Password Management**: 
  - **Hashing**: Passwords are hashed before storage, preventing their recovery even if the database is compromised.
  - **Salting**: Adds a unique salt to each password before hashing.
  - **Compliance with Strength Standards**: Ensures passwords meet specific security criteria before acceptance.
- **Security Headers**: Includes headers like X-Frame-Options, X-XSS-Protection, and Content-Security-Policy to enhance security.
