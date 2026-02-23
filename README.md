# wom-25-projekt-Del-1

A backend REST API built with Node.js and Prisma, containerized with Docker. This is Part 1 of the WOM-25 course project, focused on the server-side layer — data modeling, database access, and API endpoints. The frontend for this project lives in [wom-25-projekt-Del-2](https://github.com/thunrobi/wom-25-projekt-Del-2).

## Tech Stack

- **Runtime:** Node.js
- **Database ORM:** Prisma
- **Containerization:** Docker & Docker Compose
- **Testing:** Test suite in `test/`

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18+ recommended)
- [Docker](https://www.docker.com/) and Docker Compose
- A compatible database (configured via Prisma — see `prisma/schema.prisma`)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/thunrobi/wom-25-projekt-Del-1.git
   cd wom-25-projekt-Del-1
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Set up environment variables:**

   Create a `.env` file in the root directory and configure your database connection:

   ```env
   DATABASE_URL="your-database-connection-string"
   ```

4. **Run Prisma migrations:**

   ```bash
   npx prisma migrate dev
   ```

5. **Start the server:**

   ```bash
   npm start
   ```

### Running with Docker

To spin up the full stack using Docker Compose:

```bash
docker-compose up --build
```

This will build the application image and start all services (app + database) defined in `docker-compose.yml`.

## Project Structure

```
wom-25-projekt-Del-1/
├── prisma/          # Prisma schema and migrations
├── src/             # Backend source code (routes, controllers, etc.)
├── test/            # Test files
├── Dockerfile       # Docker image configuration
├── docker-compose.yml
└── package.json
```

## Running Tests

```bash
npm test
```

## Related

- **Part 2 (Frontend):** [wom-25-projekt-Del-2](https://github.com/thunrobi/wom-25-projekt-Del-2)

## License

This project is for educational purposes as part of the WOM-25 course.
