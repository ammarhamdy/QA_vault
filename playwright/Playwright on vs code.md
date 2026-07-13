
https://playwright.dev/docs/intro
---

# Install playwright Extensions for VS code  
[Playwright Test for VSCode](https://marketplace.visualstudio.com/items?itemName=ms-playwright.playwright)

# Install every thing that `playwight` need
```sh
npm init playwright@latest --yes "--" . '--quiet' '--browser=chromium' '--browser=firefox' '--browser=webkit' '--install-deps'
```
Or press: `Ctr` + `Shift` + `p` and type `install playwright`

---

# Project Files

Check out the following files:
- `./tests/example.spec.ts` — Example end-to-end test
- `./playwright.config.ts` — Playwright Test configuration

# Playwright Commands
Inside that directory (project directory), you can run several commands

## Run all tests inside test directory
```sh
npx playwright test
```

## `--headed` option
Run in headed mode (see browser):
```sh
npx playwright test --headed
```

## Run specific test
```sh
npx playwright test login.spec.ts
```

## `--ui` option
Runs your tests using **Playwright’s interactive Test UI** instead of just the terminal.
Use UI mode when:
- A test is failing ❌
- You’re writing new tests ✍️
- You’re unsure about selectors
```sh
npx playwright test --ui
```
It opens a graphical interface (like a mini app) provided by Playwright where you can:
- See all your test files and test cases
- Run tests individually or in groups
- Watch tests execute live in the browser
- Inspect logs, errors, and steps

## Runs the tests only on Desktop Chrome.
```sh
npx playwright test --project=chromium
```

## Runs the tests in debug mode.
```sh
npx playwright test --debug
```

## `codegen`
One of the **most powerful beginner-friendly tools** in Playwright.
It opens a browser and **records your actions**, then automatically **generates Playwright test code** for you.
```sh
npx playwright codegen
```

Open a specific website:
```sh
npx playwright codegen https://example.com
```

Save output to a file:
```sh
npx playwright codegen https://example.com -o test.spec.ts
```

