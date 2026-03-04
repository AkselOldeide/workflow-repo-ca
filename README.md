# Workflow CA

A venue booking website (Holidaze) configured with professional development tools and automated testing.

## Getting Started

### Installation

Clone the repository and install dependencies:
```bash
git clone https://github.com/YOUR-USERNAME/workflow-repo-ca.git
cd workflow-repo-ca
npm install
```

Install Playwright browsers:
```bash
npx playwright install
```

### Environment Variables

Create a `.env` file in the root of the project based on `.env.example`:
```
TEST_USER_EMAIL=
TEST_USER_PASSWORD=
```

Fill in your Noroff student credentials. This file is never committed to GitHub.

## Scripts

| Script | Command | Description |
|--------|---------|-------------|
| Dev server | `npm run dev` | Watches and compiles Tailwind CSS |
| Lint | `npm run lint` | Runs ESLint on all JS files |
| Format | `npm run format` | Runs Prettier on all files |
| Unit tests | `npm test` | Runs Vitest unit tests |
| E2E tests | `npm run test:e2e` | Runs Playwright end-to-end tests |

## Running Tests

### Unit Tests (Vitest)
```bash
npm test
```

Tests the following functions:
- `isActivePath` - validates active navigation link detection
- `getUsername` - validates user retrieval from localStorage

### End-to-End Tests (Playwright)

Start a local server first:
```bash
live-server --port=5500
```

Then in a separate terminal:
```bash
npm run test:e2e
```

Tests the following:
- User can log in with valid credentials
- User sees an error message with invalid credentials
- Navigates to a venue details page

## Development Tools

- **ESLint** - JavaScript linting with browser and test globals configured
- **Prettier** - Code formatting with single quotes, semicolons, and trailing commas
- **Husky** - Git hook that runs lint-staged before every commit
- **lint-staged** - Formats HTML files and formats + lints JavaScript files on commit
