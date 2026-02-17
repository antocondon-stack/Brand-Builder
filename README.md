# Brand Builder - Monorepo

A full-stack application for building brand identity systems with AI-powered processing.

## Project Structure

```
brand-identity-system/
├── frontend/          # Next.js — deployed to Vercel
├── backend/           # FastAPI + LangGraph — deployed to Railway
├── ingestion/         # Corpus pipeline — Railway cron job
├── .cursor/
│   └── rules          # Cursor project rules (critical)
├── .github/
│   └── workflows/     # CI/CD Actions
└── docker-compose.yml # Local dev parity
```

## Quick Start

### Prerequisites
- Node.js 18+ (for frontend)
- Python 3.9+ (for backend and ingestion)
- Docker & Docker Compose (for local development)
- Yarn (package manager)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/antocondon-stack/Brand-Builder.git
cd Brand-Builder
```

2. Install dependencies:
```bash
yarn install
```

3. Set up environment variables:
```bash
cp .env.example .env.local
```

4. Start local development:
```bash
yarn dev
```

Or use Docker Compose:
```bash
docker-compose up
```

## Available Commands

- `yarn dev` - Start frontend and backend in development mode
- `yarn build` - Build all workspaces
- `yarn lint` - Lint all workspaces
- `yarn test` - Run tests in all workspaces
- `yarn workspace <name> <command>` - Run command in specific workspace

## Workspaces

### Frontend (`frontend/`)
Next.js application with React. Deployed to Vercel.

```bash
yarn workspace frontend dev
```

### Backend (`backend/`)
FastAPI + LangGraph service. Deployed to Railway.

```bash
yarn workspace backend dev
```

### Ingestion (`ingestion/`)
Corpus pipeline and data ingestion. Runs as Railway cron job.

```bash
yarn workspace ingestion dev
```

## Development Setup

### Using Docker Compose
```bash
docker-compose up
```

This will start all services locally and ensure parity with production.

### Environment Variables
See `.env.example` for required environment variables.

## CI/CD

GitHub Actions workflows are configured in `.github/workflows/`. See that directory for:
- Linting and testing
- Building and deployment
- Automated checks

## Cursor Configuration

Project-specific Cursor rules are in `.cursor/rules`. These should be reviewed and maintained.

## Contributing

1. Create a feature branch
2. Make your changes
3. Run tests and linting: `yarn test && yarn lint`
4. Submit a pull request

## License

[Add your license here]

## Support

[Add support contact information]