# Expense Tracker Backend

## Introduction
This is the backend part of the application, built using Node.js and Express. The backend is responsible for handling API requests, managing data storage, and ensuring secure and efficient communication between the client and server.

## Features
- RESTful API design
- Data validation and sanitization
- MongoDB database integration for data storage
- Secure data handling with environment variables
- Error handling and logging
- Postman collection included for API testing

## Technologies Used
- **Node.js**: JavaScript runtime built on Chrome's V8 JavaScript engine.
- **Express.js**: Minimal and flexible Node.js web application framework.
- **MongoDB**: NoSQL database for storing and managing application data.
- **Mongoose**: ODM (Object Data Modeling) library for MongoDB and Node.js.
- **dotenv**: To manage environment variables.

## Getting Started
1. **Clone the repository**:
```bash
   git clone https://github.com/alihdede7/FinTracker.git
```
2. **Navigate to the backend directory**:
```bash
   cd FinTracker/backend
```
4. **Install dependencies**:
```bash
   npm install
```
5. **Set up environment variables**:
   1. Create a `.env` file in the root of the backend directory.
   2. Add the following environment variables:
      
        - **PORT**=`your_port_number`
        - **MONGO_URL**=`your_mongo_connection_string`

   
6. **Run the application**:
```bash
   npm start
```
## License
This project is licensed under the MIT License. See the LICENSE file for details.


