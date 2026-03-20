# Database Schema

## Users Table

Stores user information.

| Column Name | Data Type    | Constraints               | Description    |
| ----------- | ------------ | ------------------------- | -------------- |
| id          | SERIAL       | PRIMARY KEY               | Unique user ID |
| name        | VARCHAR(100) | NOT NULL                  | User name      |
| email       | VARCHAR(100) | UNIQUE, NOT NULL          | User email     |
| created_at  | TIMESTAMP    | DEFAULT CURRENT_TIMESTAMP | Created time   |

---

## Orders Table

Stores user orders.

| Column Name | Data Type     | Constraints               | Description    |
| ----------- | ------------- | ------------------------- | -------------- |
| id          | SERIAL        | PRIMARY KEY               | Order ID       |
| user_id     | INT           | FK → users(id), NOT NULL  | User reference |
| amount      | DECIMAL(10,2) | NOT NULL                  | Order amount   |
| created_at  | TIMESTAMP     | DEFAULT CURRENT_TIMESTAMP | Created time   |
