# Document Store Model

## 1. Users Collection

### User Document
- `_id`: Unique identifier (e.g., ObjectId)
- `username`: String
- `email`: String
- `password`: String (hashed for security)
- `role`: String (e.g., "user" or "admin")

## 2. Categories Collection

### Category Document
- `_id`: Unique identifier (e.g., ObjectId)
- `name`: String
- `type`: String (e.g., "income" or "expense")
- `description`: String

## 3. Transactions Collection

### Transaction Document
- `_id`: Unique identifier (e.g., ObjectId)
- `userId`: Reference to the Users collection
- `categoryId`: Reference to the Categories collection
- `date`: Date
- `amount`: Number
- `description`: String
- `type`: String (e.g., "income" or "expense")

## 4. Budgets Collection

### Budget Document
- `_id`: Unique identifier (e.g., ObjectId)
- `userId`: Reference to the Users collection
- `categoryId`: Reference to the Categories collection
- `startDate`: Date
- `endDate`: Date
- `amount`: Number

## 5. Reports Collection

### Report Document
- `_id`: Unique identifier (e.g., ObjectId)
- `userId`: Reference to the Users collection
- `startDate`: Date
- `endDate`: Date
- `income`: Number
- `expense`: Number
- `balance`: Number

## Rationale

- **Users Collection**: Stores information about registered users, including their username, email, password, and role.
- **Categories Collection**: Stores the different categories for transactions, such as "Food" or "Transportation".
- **Transactions Collection**: Stores individual transactions, including the user who made the transaction, the category, date, amount, and description.
- **Budgets Collection**: Stores budget information for each user, including the category, start and end dates, and allocated amount.
- **Reports Collection**: Stores generated reports for each user, including the start and end dates, income, expense, and balance.

## Indexing

- Indexes to be created on the `userId` fields in the Transactions, Budgets, and Reports collections to facilitate fast lookup and aggregation of data by user.
- Indexes to be created on the `categoryId` fields in the Transactions and Budgets collections to facilitate fast lookup and aggregation of data by category.
- Compound indexes to be created on the `startDate` and `endDate` fields in the Budgets and Reports collections to facilitate fast range queries.
