# Content Management System (CMS)

## Introduction
This project is a **Content Management System (CMS) API** designed to manage articles and categories efficiently. The system provides authentication, role-based access control, advanced search functionality, interactions, caching, and logging mechanisms.

## Features

### 1. User Management & Authentication
- **JWT Authentication** for secure login.
- **OAuth2 Support** for Google account integration.
- **Roles & Permissions:**
  - **Admin:** Manage all users, articles, categories, and settings.
  - **Editor:** Create, edit, and delete articles.
  - **Author:** Create and edit own articles.
  - **User:** Read and comment on articles.
- **Security Enhancements:**
  - Rate Limiting to prevent brute-force attacks.
  - Two-Factor Authentication (2FA).
  - Notifications for new device logins.

### 2. Article & Category Management
- Articles include:
  - Title, content, category, keywords, status, view count, and reading stats.
  - Auto image compression & upload support.
  - Advanced search via **Elasticsearch** or **Meilisearch**.
- Supports **nested categories** and **tags system**.

### 3. Advanced Search & Categorization
- Smart search functionality.
- Filter articles by **popularity, latest, and top-rated**.
- Personalized recommendations based on user reading history.

### 4. User Interactions & Comments
- **Nested comments** (threaded discussion support).
- Like/Dislike feature for articles and comments.
- Report inappropriate comments.

### 5. Performance Optimization
- **Redis Caching** for faster article loading.
- Auto image compression.
- **SEO Optimizations** using **JSON-LD & Meta Tags**.

### 6. API Documentation
- API documented using **Swagger** or **Postman**.
- Provides **Postman Collection** for easy testing.

### 7. Activity Logging & Monitoring
- Logs all user actions using an **Activity Log**.
- Dashboard for monitoring top articles and most active users.

## API Endpoints

### 1. User Management
- `POST /api/register` → Register a new user.
- `POST /api/login` → User login.
- `POST /api/logout` → User logout.
- `POST /api/reset-password` → Reset password.
- `POST /api/verify-2fa` → Verify Two-Factor Authentication.

### 2. Article Management
- `GET /api/articles` → Get all articles.
- `GET /api/articles/{id}` → Get a specific article.
- `POST /api/articles` → Create a new article.
- `PUT /api/articles/{id}` → Update an article.
- `DELETE /api/articles/{id}` → Delete an article.

### 3. Category Management
- `GET /api/categories` → Get all categories.
- `POST /api/categories` → Create a new category.

### 4. Search & Categorization
- `GET /api/search?q=keyword` → Search for articles.
- `GET /api/articles/popular` → Get most viewed articles.
- `GET /api/articles/recommended` → Get personalized recommendations.

### 5. Comments & Interactions
- `POST /api/comments/{article_id}` → Add a comment.
- `PUT /api/comments/{id}` → Edit a comment.
- `DELETE /api/comments/{id}` → Delete a comment.
- `POST /api/comments/{id}/like` → Like a comment.
- `POST /api/comments/{id}/report` → Report a comment.

### 6. Performance Optimization
- `GET /api/cache/articles` → Get cached articles.
- `DELETE /api/cache/articles` → Clear article cache.

### 7. Activity Logging
- `GET /api/logs` → View all activities.
- `GET /api/analytics` → View system analytics.

## Task Submission Process

### Steps to Submit a Task:
1. **Fork the main repository:**  
   Repository: [task-web-crud-ContentManagementSystem](https://github.com/IT-Club-Workspace/task-web-crud-ContentManagementSystem.git)
2. **Clone the repository to your local machine:**
   ```sh
   git clone https://github.com/YOUR_USERNAME/task-web-crud-ContentManagementSystem.git
   ```
3. **Create a folder with your name and seat number:**  
   Format: `[member_name]_[seat_number]`
   - Example: `Ahmed_Ali_2220140`
4. **Place your task-related files inside your folder.**
5. **Commit and push your changes:**
   ```sh
   git add .
   git commit -m "Added my task"
   git push origin main
   ```
6. **Create a Pull Request (PR) to the main repository.**
7. **Code Review & Approval:**
   - The task will be reviewed by the project supervisors.
   - Feedback or modification requests may be provided.
   - Tasks that do not meet the requirements will be rejected with suggestions for improvement.

## Contribution Guidelines
- Follow clean coding standards.
- Use meaningful commit messages.
- Write detailed documentation where necessary.
- Ensure API endpoints follow RESTful best practices.
- Test your code before submitting.

---
By contributing to this project, you agree to follow the **community guidelines** and **maintain code quality** to ensure the project's success. 🚀
