# Notes App Backend

A RESTful API backend for managing notes built with Hapi.js framework.

## Features

- Create, read, update, and delete notes
- In-memory storage
- CORS enabled
- RESTful API endpoints

## Prerequisites

- Node.js (version 14 or higher)
- npm

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```

## Usage

### Development
```bash
npm run start:dev
```

### Production
```bash
npm run start:prod
```

### Linting
```bash
npm run lint
```

The server will run on `http://localhost:5000`

## API Endpoints

### Create Note
- **POST** `/notes`
- **Body:**
  ```json
  {
    "title": "Note title",
    "tags": ["tag1", "tag2"],
    "body": "Note content"
  }
  ```

### Get All Notes
- **GET** `/notes`

### Get Note by ID
- **GET** `/notes/{id}`

### Update Note
- **PUT** `/notes/{id}`
- **Body:**
  ```json
  {
    "title": "Updated title",
    "tags": ["updated", "tags"],
    "body": "Updated content"
  }
  ```

### Delete Note
- **DELETE** `/notes/{id}`

## Dependencies

- **@hapi/hapi**: Web framework
- **nanoid**: Unique ID generator

## Development Dependencies

- **eslint**: Code linting
- **nodemon**: Development server with auto-restart

## Testing

Postman collection and environment files are included for API testing:
- `notes-api-test.postman_collection.json`
- `notes-api-test.postman_environment.json`