<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg" alt="Donate us"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

# Backend NestJS API

This is a backend API built using the [NestJS](https://nestjs.com/) framework. It provides a robust and scalable server-side application for managing users, products, orders, categories, and more. The API is designed with modularity, security, and extensibility in mind.

## Features

- **User Management**: Create, update, delete, and retrieve user information.
- **Product Management**: Manage products with categories, stock, and images.
- **Order Management**: Handle orders with associated details and users.
- **Category Management**: Organize products into categories.
- **Authentication and Authorization**: Secure endpoints with JWT-based authentication and role-based access control.
- **Cloudinary Integration**: Upload and manage product images using Cloudinary.
- **Swagger Documentation**: Interactive API documentation with Swagger.
- **Database Integration**: PostgreSQL database with TypeORM for ORM.

## Prerequisites

- [Node.js](https://nodejs.org/) (v20.18.0 or higher)
- [PostgreSQL](https://www.postgresql.org/) (configured in `.env` file)
- [Docker](https://www.docker.com/) (optional, for containerized setup)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Backend_NestJs_Api/back
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   - Create a `.env.development` file in the root directory.
   - Add the following variables:
     ```
     DB_HOST=localhost
     DB_PORT=5432
     DB_USERNAME=your_db_username
     DB_PASSWORD=your_db_password
     DB_NAME=your_db_name
     JWT_SECRET=your_jwt_secret
     CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
     CLOUDINARY_API_KEY=your_cloudinary_api_key
     CLOUDINARY_API_SECRET=your_cloudinary_api_secret
     ```

4. Run database migrations (if applicable):
   ```bash
   npm run typeorm migration:run
   ```

## Running the Application

### Development Mode

```bash
npm run start:dev
```

The application will run on `http://localhost:3000`.

### Production Mode

1. Build the application:
   ```bash
   npm run build
   ```

2. Start the application:
   ```bash
   npm run start:prod
   ```

### Using Docker

1. Build and start the containers:
   ```bash
   docker-compose up --build
   ```

2. The application will be available at `http://localhost:3001`.

## API Documentation

The API is documented using Swagger. Once the application is running, you can access the documentation at:

```
http://localhost:3000/api
```

## Testing

### Unit Tests

Run unit tests:
```bash
npm run test
```

### End-to-End Tests

Run e2e tests:
```bash
npm run test:e2e
```

### Test Coverage

Generate test coverage report:
```bash
npm run test:cov
```

## Project Structure

- **`src/modules`**: Contains feature modules (e.g., users, products, orders).
- **`src/helpers`**: Utility functions and services.
- **`src/migrations`**: Database migration files.
- **`src/main.ts`**: Application entry point.
- **`test`**: Contains e2e test files.

## Deployment

For deployment, ensure the following:

1. Set `NODE_ENV=production` in your environment variables.
2. Use a production-ready database (e.g., AWS RDS, Azure Database).
3. Build the application:
   ```bash
   npm run build
   ```
4. Start the application:
   ```bash
   npm run start:prod
   ```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your message here"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, please contact:

- **Author**: [Your Name]
- **Email**: [Your Email]
- **Website**: [Your Website]
