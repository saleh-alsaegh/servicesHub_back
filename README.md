# ServicesHub Backend API

A REST API for a services marketplace platform that connects customers with service providers. The API enables users to create service requests, categorize services, and facilitate communication between customers and providers through comments and interest indicators.

## Technologies Used

- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT (jsonwebtoken)** - Authentication tokens
- **bcrypt** - Password hashing
- **CORS** - Cross-origin resource sharing
- **Morgan** - HTTP request logging

## Installation

1. Clone the repository
2. Install dependencies: `npm install`
3. Create a `.env` file with: MONGODB_URI, SESSION_SECRET, SALT_ROUNDS, PORT
4. Start the server: `npm start`

## API Features

- **Authentication**: Sign up, sign in with JWT tokens
- **User Roles**: Service Provider and Customer types
- **Categories**: Service providers can create/manage service categories
- **SubCategories**: Service providers can create/manage subcategories
- **Requests**: Users can create service requests with comments and "can do" interactions
- **Authorization**: Role-based permissions and resource ownership validation

## Key API Endpoints

- **Authentication**: `/api/auth` - signup, signin, profile management
- **Categories**: `/api/categories` - service category management (service providers only)
- **SubCategories**: `/api/subcategories` - subcategory management (service providers only)
- **Requests**: `/api/requests` - service request management with comments and interactions

## Authorization

- Service providers can create/edit categories and subcategories
- All authenticated users can create requests and interact with them
- Users can only modify their own content
