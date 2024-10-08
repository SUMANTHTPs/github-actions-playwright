# Playwright Sample Tests

This repository contains sample tests using Playwright for end-to-end testing.

## Prerequisites

- Node.js (>= 20.14.12)
- npm (>= 6.x) or yarn (>= 1.x)

## Setup

### 1. Clone the Repository

```bash
git clone https://github.com/SUMANTHTPs/Playwright-sample-tests.git
cd Playwright-sample-tests
```
- Change directory based on your path

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Update credentials in config.yml

```bash
url: "https://www.amazon.in/"
email: ""
password: ""
```

## Running Tests

#### To run tests in parallel mode, Increase workers in `playwright.config.ts`

### 1. Run All Tests

To run all the tests in the project:

```bash
npx playwright test
# or
yarn playwright test
```

### 2. Run Tests with a Specific Configuration

To run tests with a specific configuration, use the `--config` option:

```bash
npx playwright test --config=playwright.config.ts
# or
yarn playwright test --config=playwright.config.ts
```

### 3. Run Tests for a Specific Project

To run tests for a specific project defined in the configuration:

```bash
npx playwright test --project=Login
# or
yarn playwright test --project=Login
```

### 4. Run a Specific Test File

To run a specific test file:

```bash
npx playwright test tests/login.test.ts
# or
yarn playwright test tests/login.test.ts
```

## Additional Commands

### Update Playwright Browsers

To ensure you have the latest browser binaries:

```bash
npx playwright install
# or
yarn playwright install
```

### Generate Test Reports

Playwright can generate test reports in various formats:

```bash
npx playwright show-report
# or
yarn playwright show-report
```

## Project Structure

```
.
├── artifacts
│   ├── ... all test artifacts
├── authArtifacts
│   ├── storageState.json
├── src
│    ├── pages
│    │   ├── landingPage.page.ts
│    │   ├── products.page.ts
│    │   └── ...
│    ├── tests
│    │   ├── login.test.ts
│    │   ├── search.test.ts
│    │   └── ...
│    └── utils
│        └── testUtils.ts
│        └── constants.ts
│        └── selectors.ts
├── playwright.config.ts
├── config.yml
├── package.json
└── README.md
```

## Notes

- Ensure the correct Node.js version is installed. You can use tools like `nvm` to manage Node.js versions.
- Refer to the Playwright [documentation](https://playwright.dev/docs/intro) for more details on configuration and usage.