# Node Express Boilerplate

This repository contains a boilerplate for building Node.js applications with Express. The project provides a minimal setup to get started with Express and TypeScript.

## Repository Structure

The repository is organized as follows:

- **src/**: Source code directory
  - **server.ts**: Main server file with Express configuration
  - **utils/**: Utility functions
    - **handleError.ts**: Error handling utility

- **.gitignore**: Git ignore file
- **nodemon.json**: Nodemon configuration for development
- **package.json**: Project dependencies and scripts
- **tsconfig.json**: TypeScript configuration

## Features

The Node Express Boilerplate offers the following features:

- **TypeScript Integration**
  - Full TypeScript support
  - Type-safe Express application

- **Express Server**
  - Pre-configured Express server
  - Basic routing setup

- **Error Handling**
  - Centralized error handling utility
  - Consistent error responses

- **Development Tools**
  - Nodemon for automatic server restart during development
  - Environment variable support with dotenv

## How to Use

1. **Installation**:
   ```bash
   npm install
   ```

2. **Running the Server**:
   - Development mode:
     ```bash
     npm run dev
     ```
   - Production mode:
     ```bash
     npm run build
     npm start
     ```

3. **Environment Variables**:
   - Create a `.env` file in the root directory
   - Define your environment variables (e.g., `PORT=3000`)

## API Endpoints

- **GET /** - Returns a "Hello, world!" message

## Technical Implementation

The application is built using:
- Node.js for the runtime environment
- Express.js for the web framework
- TypeScript for type safety
- dotenv for environment variable management

## Requirements

- Node.js (v14 or higher recommended)
- npm or yarn package manager

## Getting Started

To use this boilerplate:

1. Clone this repository
2. Install dependencies with `npm install`
3. Start the development server with `npm run dev`
4. Access the server at `http://localhost:3000`

## Extending the Boilerplate

This boilerplate is designed to be minimal and extensible. Here are some suggestions for extending it:

- Add middleware for authentication, logging, etc.
- Implement a database connection (MongoDB, PostgreSQL, etc.)
- Create additional routes and controllers
- Add testing with Jest or Mocha

---

*This boilerplate provides a solid foundation for building robust Node.js applications with Express and TypeScript.*