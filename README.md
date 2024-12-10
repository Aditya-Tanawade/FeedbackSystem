
# Feedback and Review System

This is a simple feedback and review system that allows users to submit ratings and comments. Admins can approve, delete, or manage reviews, and the system displays average ratings for each product or service.

## Features

### User Features:
- Submit feedback with ratings and comments.
- View product/service reviews and average ratings.

### Admin Features:
- Approve or delete user reviews.
- View a list of all reviews with details like rating, comment, and approval status.

### System Features:
- Real-time updates of review approval status.
- Display of average ratings for products or services.

## Tech Stack

- **Backend**: Spring Boot
- **Frontend**: React
- **Database**: H2 (in-memory database, can be replaced with MySQL, PostgreSQL, etc.)
- **Authentication**: Optional (if implementing user/admin login)
- **State Management**: React State or Redux (optional, for complex state management)

## Project Structure

```
.
├── backend/
│   ├── src/
│   ├── pom.xml              # Spring Boot dependencies
│   └── application.properties  # Configuration files
└── frontend/
    ├── src/
    ├── package.json         # React dependencies
    └── public/
```

## Requirements

- **Java 11** or higher
- **Node.js** and **npm** (for React)
- **Maven** or **Gradle** (for Spring Boot)
- **Database** (H2, MySQL, etc.)

## Setup Instructions

### Backend (Spring Boot)

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Aditya-Tanawade/FeedbackSystem.git
   ```

2. **Navigate to the backend directory** (make sure you're inside the project folder):
   ```bash
   cd feedback-review-system/backend
   ```

3. **Build the backend**:
   Make sure you have Maven installed. You can build the project using the following command:
   ```bash
   ./mvnw clean install
   ```
   This will install all the required dependencies for the backend.

4. **Run the Spring Boot application**:
   After building the project, you can run the Spring Boot application with:
   ```bash
   ./mvnw spring-boot:run
   ```
   The Spring Boot API will be running on `http://localhost:8080`.

### Frontend (React)

1. **Navigate to the frontend directory**:
   ```bash
   cd feedback-review-system/frontend
   ```

2. **Install dependencies**:
   First, install all the required dependencies for React:
   ```bash
   npm install
   ```

3. **Start the React development server**:
   Run the React application:
   ```bash
   npm start
   ```
   The React application will be running on `http://localhost:3000`.

## API Endpoints

### User Endpoints:
- **GET** `/api/reviews`: Get all reviews.
- **POST** `/api/reviews`: Submit a new review (rating, comment).

### Admin Endpoints:
- **GET** `/api/admin/reviews`: Get all reviews (including pending approval).
- **PUT** `/api/admin/reviews/{id}/approve`: Approve a review.
- **DELETE** `/api/admin/reviews/{id}`: Delete a review.

## Database Schema

### Review Table

| Column      | Type          | Description                             |
|-------------|---------------|-----------------------------------------|
| `id`        | Long          | Unique ID for the review               |
| `rating`    | Integer       | Rating (1-5)                           |
| `comment`   | String        | User's review comment                  |
| `status`    | String        | Review status (approved, pending)      |
| `createdAt` | LocalDateTime | Timestamp when the review was created  |

## Admin Panel

Admins can access the admin panel through a protected route and manage reviews. Features include:
- Review approval.
- Review deletion.
- Viewing ratings and comments.

## Running the Application

1. **Backend**: Make sure your Spring Boot application is running on port `8080`.
2. **Frontend**: The React application will be available at `http://localhost:3000`.

### Notes:
- You can configure different database options by editing `application.properties` in the Spring Boot backend.
- Make sure to adjust any CORS or security configurations as needed for communication between the frontend and backend.

3. **Commit the Changes**: After pasting the content into the file, scroll down to the "Commit changes" section and add a commit message. Click the "Commit changes" button to save it.

---

This will structure your README with clear sections, API endpoint documentation, and step-by-step instructions for running both the backend and frontend. Let me know if you need further adjustments!
