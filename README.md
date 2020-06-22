# Secure Banking System

An online banking system 

### Features:

- Functional:
  - Transactions
    - Deposit
    - Withdrawal
  - Account Management
    - Account Creation
    - Account Modification
    - Account Deletion
  - Two Factor Authentication through OTPs
  - View Event Logs
  - Schedule Appointments

- Security:
  - Two Factor Authentication for transactions above a configurable amount (termed critical transactions).
  - Tiering of Users to enforce restricted access to certain functionalities. The different tiers are:
    - Tier 1 User (Customers):
      - Deposit / Withdraw amount
      - Raise requests for new account, changes to account to Tier 2 Users.
      - Schedule Appointments with Tier 2 Users.
    - Tier 2 User (Bank Employees):
      - Approve / Decline critical transactions.
      - Approve / Decline requests related to accounts
      - Handle appointments.
    - Tier 3 User (System Admins):
      - User Management (create, modify, delete user personal and login info)
      - View Event Logs
  - SSL / HTTPS certificates for trusted access.
  - Handle XSS (Cross-site scripting attacks).
  - Secure communication using REST API Auth tokens.

### Architecture:

#### FrontEnd
User Interface for performing user actions. Implemented using Vue.js, a Javascript based framework.

#### BackEnd
REST APIs and Backend APIs implemented using Java Spring framework, with Hibernate as the ORM framework.

#### Persistence Layer
MySQL database with a normalized schema design.

#### Deployment
Apache Tomcat deployable on local and cloud architectures like AWS.
