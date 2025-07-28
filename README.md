# Event Management Platform API

A modern, fast, and scalable API for event management built with FastAPI, SQLAlchemy, and Poetry.

## Features

- 🚀 **FastAPI** - Modern, fast web framework for building APIs
- 🐍 **Python 3.13** - Latest Python version for optimal performance
- 📦 **Poetry** - Dependency management and packaging
- 🗄️ **SQLAlchemy** - SQL toolkit and ORM
- 🔄 **Alembic** - Database migrations
- 🔒 **JWT Authentication** - Secure token-based authentication
- 🧪 **Testing** - Comprehensive test suite with pytest
- 🎨 **Code Quality** - Ruff, Black, and isort for code formatting
- 📝 **Type Checking** - MyPy for static type checking

## Prerequisites

- Python 3.13+
- Poetry (installed automatically)

## Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd event-management-platform-API-
   ```

2. **Install dependencies:**
   ```bash
   poetry install
   ```

3. **Set up environment variables:**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

## Development

### Running the Application

```bash
# Using Poetry
poetry run python run.py

# Or activate the virtual environment first
poetry shell
python run.py
```

The API will be available at `http://localhost:8000`

### API Documentation

- **Swagger UI**: `http://localhost:8000/docs`
- **ReDoc**: `http://localhost:8000/redoc`

### Code Quality

```bash
# Format code
poetry run black .
poetry run isort .

# Lint code
poetry run ruff check .

# Type checking
poetry run mypy .

# Run all checks
poetry run ruff check . && poetry run black --check . && poetry run isort --check-only .
```

### Testing

```bash
# Run tests
poetry run pytest

# Run tests with coverage
poetry run pytest --cov=app

# Run tests with verbose output
poetry run pytest -v
```

## Project Structure

```
event-management-platform-API-/
├── app/
│   ├── api/          # API routes and endpoints
│   ├── core/         # Core functionality (config, security)
│   ├── db/           # Database models and sessions
│   ├── models/       # SQLAlchemy models
│   ├── schemas/      # Pydantic schemas
│   ├── services/     # Business logic
│   └── utils/        # Utility functions
├── tests/            # Test files
├── pyproject.toml    # Poetry configuration
├── run.py           # Application entry point
└── README.md        # This file
```

## Configuration

The application uses Pydantic Settings for configuration. Key settings include:

- `DATABASE_URL`: PostgreSQL connection string
- `SECRET_KEY`: JWT secret key
- `ALLOWED_HOSTS`: CORS allowed origins
- `ENVIRONMENT`: Environment (development/staging/production)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run code quality checks
5. Add tests for new functionality
6. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.