# Todo App

A simple, modern todo application built with React Router v7.

## Tech Stack

- **Framework**: React Router v7
- **Runtime**: Node.js
- **Database**: SQLite  
- **Testing**: Vitest (unit tests), Playwright (E2E tests)
- **Deployment**: Cloudflare Workers
- **Package Manager**: npm

## Project Structure

- `app/`: React Router v7 application code
  - `routes/`: Route components and handlers
  - `components/`: Reusable React components
  - `lib/`: Utilities and database client
  - `types/`: TypeScript type definitions
- `tests/`: Test files
- `playwright/`: E2E test configurations
- `migrations/`: Database migration files

## Commands

- `npm run dev`: Start development server
- `npm run build`: Build for production
- `npm run test`: Run unit tests with Vitest
- `npm run test:e2e`: Run E2E tests with Playwright
- `npm run typecheck`: Run TypeScript checker
- `npm run lint`: Run ESLint
- `npm run deploy`: Deploy to Cloudflare Workers

## Code Style

- Use TypeScript strict mode
- Prefer function components with hooks
- Use ES modules (import/export) syntax
- Follow naming conventions:
  - PascalCase for components
  - camelCase for functions and variables
  - kebab-case for file names
- Use React Router v7 conventions for routing and data loading

## Database

- SQLite database with migrations
- Use Drizzle ORM for type-safe database queries
- Keep database schema in `app/lib/schema.ts`
- Run migrations before deployment

## Testing

- Unit tests with Vitest for components and utilities
- E2E tests with Playwright for user workflows
- Test files should be co-located with source files (`.test.ts` suffix)
- Aim for comprehensive coverage of todo CRUD operations

## Deployment

- Deploy to Cloudflare Workers using Wrangler
- Database runs on Cloudflare D1
- Environment variables configured in `wrangler.toml`
- Automatic deployments on main branch push

## Features

Core todo functionality:
- Add new todos
- Mark todos as complete/incomplete
- Edit todo text
- Delete todos
- Filter todos (all, active, completed)
- Clear completed todos

## Do Not

- Do not use class components
- Do not commit environment files
- Do not skip TypeScript types
- Do not deploy without running tests
- Do not modify database schema without migrations

## Development Workflow

- Run typecheck and lint after completing tasks and be sure they ALWAYS pass