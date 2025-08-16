<h1 align="center">Eduva Backend</h1>
<p align="center">
    <img src="documents/eduva-logo.png" alt="Logo" height="128" width="128"/>
</p>
<p align="center">
    Backend for AI-Powered Learning Material Management System with Automated Audio/Video Lesson Generation for High School Teachers
</p>

<a name="table-of-contents"></a>

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Description](#description)
- [Installation](#installation)
  - [Requirements](#requirements)
  - [Clone the Project](#clone-the-project)
  - [Environment Setup](#environment-setup)
  - [Running the Application](#running-the-application)
- [Project Structure](#project-structure)
- [TODO](#todo)
- [License](#license)

<a name="description"></a>

## Description

Eduva Backend is the core service for the AI-powered learning material management system. It provides APIs and backend logic for managing educational content, automating the generation of audio/video lessons, and supporting high school teachers in their teaching process.

#### 🧠 AI Lesson Generation Page

![Screenshot of AI lesson generation page](documents/eduva-screenshot-ai.png)

#### 🏫 School Dashboard

![Screenshot of school dashboard page](documents/eduva-screenshot-school-dashboard.png)

#### 📚 Lesson Management

![Screenshot of lesson management page](documents/eduva-screenshot-lesson-management.png)

<a name="installation"></a>

## Installation

<a name="requirements"></a>

### Requirements

- .NET 8.0 SDK (for backend)
- PostgreSQL (database, required for backend)
- Redis (cache, required for backend)
- RabbitMQ (message broker, required for backend)
- Azure Blob Storage (for file storage, required for backend)
- Docker & Docker Compose (optional, for local development and deployment)

<a name="clone-the-project"></a>

### Clone the Project

```bash
git clone https://github.com/tranduckhuy/eduva-backend.git
cd eduva-backend/backend
```

<a name="environment-setup"></a>

### Environment Setup

- Copy `.env.example` to `.env` and fill in your environment variables for local development or Docker Compose.
- For .NET local development, use the .NET Secret Manager to store sensitive values in `secrets.json` (see [documents/environment-setup.md](documents/environment-setup.md) for details and example structure).
- **Do not commit `.env` or `secrets.json` with real credentials to source control.**

<a name="running-the-application"></a>

### Running the Application

```bash
cd backend/src/Eduva.API
dotnet restore
dotnet build
dotnet run
```

Or with Docker Compose:

```bash
docker-compose -f docker-compose.yaml -f docker-compose.override.yaml up --build
```

<a name="project-structure"></a>

## Project Structure

```
backend/
  src/
    Eduva.API/           # API project
    Eduva.Application/   # Application logic
    Eduva.Domain/        # Domain models
    Eduva.Infrastructure/# Infrastructure and data access
    Eduva.Shared/        # Shared resources
  tests/                 # Unit and integration tests
```

<a name="todo"></a>

## TODO

- [ ] Implement more AI-powered features

<a name="license"></a>

## License

See [LICENSE](LICENSE) for details.
