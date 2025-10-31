# Know Your Neighbor

A Node.js web application built with Express.js that helps community members connect, share local store information, and plan weekend activities. The app features user authentication, store management, and weekend planning capabilities.

## Features

- **User Authentication**: Register and login functionality with secure password hashing
- **Store Management**: Add and view local stores with descriptions, locations, and images
- **Weekend Planning**: Create and save weekend activity plans
- **Community Focus**: Connect neighbors through shared local information
- **Responsive Design**: Clean, user-friendly interface

## Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: bcryptjs for password hashing, express-session for session management
- **Frontend**: HTML, CSS, JavaScript
- **Containerization**: Docker
- **Orchestration**: Kubernetes

## Prerequisites

- Node.js (v14 or higher)
- MongoDB (local installation or MongoDB Atlas)
- Docker (for containerized deployment)
- kubectl (for Kubernetes deployment)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd know-your-neighbor
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up MongoDB:
   - Install MongoDB locally or use MongoDB Atlas
   - Update the connection string in `app.js` if needed

4. Start the application:
   ```bash
   npm start
   ```

5. Open your browser and navigate to `http://localhost:3000`

## Usage

### User Registration and Login
- Visit the registration page to create a new account
- Login with your credentials to access the application

### Adding Stores
- Navigate to the "Add Store" page
- Fill in store details including name, description, location, and image URL
- Submit to save the store to the database

### Weekend Planning
- Use the weekend planner to add activities for Saturday and Sunday
- Save your plans for future reference

### Viewing Data
- Access the store page to view all saved stores
- Check weekend events to see planned activities

## API Endpoints

- `GET /` - Home page
- `GET /index` - Main application page
- `GET /login` - Login page
- `GET /register` - Registration page
- `POST /register` - User registration
- `POST /login` - User login
- `GET /add-store` - Add store page
- `POST /add-store` - Save new store
- `GET /store` - View stores page
- `GET /weekend-events` - Weekend events page
- `POST /weekend-plan` - Save weekend plan
- `GET /api/savedData` - Retrieve all saved stores and weekend plans

## Deployment

### Docker

1. Build the Docker image:
   ```bash
   docker build -t know-your-neighbor .
   ```

2. Run the container:
   ```bash
   docker run -p 3000:3000 know-your-neighbor
   ```

### Kubernetes

1. Apply the Kubernetes manifests:
   ```bash
   kubectl apply -f k8s/
   ```

2. Check the deployment status:
   ```bash
   kubectl get pods
   kubectl get services
   ```

## Project Structure

```
know-your-neighbor/
├── app.js                 # Main application file
├── package.json           # Dependencies and scripts
├── Dockerfile             # Docker configuration
├── k8s/                   # Kubernetes manifests
│   ├── deployment.yaml
│   └── service.yaml
├── css/                   # Stylesheets
├── js/                    # Client-side JavaScript
├── img/                   # Images
├── *.html                 # HTML pages
└── README.md              # Project documentation
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.
