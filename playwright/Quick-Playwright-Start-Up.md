
```sh
# Creates a package.json in the current folder using default values (-y = "yes to all prompts").
# Produces: package.json (project name, version, scripts, dependencies list).
# Needed: first step so npm can track your project's dependencies and scripts.
npm init -y

# Runs Playwright's official setup wizard (downloads the latest init tool via npx).
# Asks: language (TypeScript/JavaScript), tests folder name, GitHub Actions workflow, browser install.
# Produces:
#   - playwright.config.ts          -> main test configuration
#   - tests/example.spec.ts         -> sample test
#   - tests-examples/               -> extra demo tests
#   - .github/workflows/playwright.yml (if you chose CI)
#   - @playwright/test added to devDependencies in package.json
#   - Browser binaries (if you accepted the install prompt)
# Needed: bootstraps the whole framework, so you don't configure everything by hand.
npm init playwright@latest

# Downloads the browser binaries Playwright drives (Chromium, Firefox, WebKit).
# Produces: browsers stored in a local cache (e.g. ~/.cache/ms-playwright on Linux),
#           not inside your project folder.
# Needed: tests cannot run without these browsers. Run it again after upgrading
#         Playwright, on a fresh machine, or in CI (use `--with-deps` on Linux CI
#         to also install required OS libraries).
npx playwright install
```
Note: `npm init playwright@latest` can already install browsers if you accept the prompt, so `npx playwright install` is only required if you skipped that step, upgraded Playwright, or are setting up a new machine/CI runner.


```sh
# Runs all tests headless, in parallel, across every project in playwright.config.ts.
# Produces: terminal output + HTML report folder (playwright-report/) + test-results/ for failures.
npx playwright test

# Opens the last HTML report in your browser (results, traces, screenshots, videos).
# Needed: to inspect failures after a run.
npx playwright show-report

# Runs tests with a visible browser window instead of headless.
# Needed: to watch what the test does while developing.
npx playwright test --headed

# Runs only the tests in the matching file (partial name match works).
# Needed: fast feedback while working on a single spec.
npx playwright test login.spec.ts

# Opens UI Mode: a visual runner with test list, timeline, watch mode, and time-travel debugging.
# Needed: best tool for authoring and investigating tests interactively.
npx playwright test --ui

# Runs tests in debug mode: headed browser, Playwright Inspector, step-by-step execution.
# Needed: to pause, step through actions, and inspect locators when a test fails.
npx playwright test --debug

# Opens a browser and records your clicks/typing as test code (generated live in the Inspector).
# Needed: quickly generate locators and a starting test; always review and refactor the output.
npx playwright codegen https://example.com

# Runs a single test by its title instead of the whole file.
npx playwright test -g "should login successfully"

# Runs in one browser project only (name from playwright.config.ts).
npx playwright test --project=chromium

# Opens a recorded trace file to replay a failed test step by step.
npx playwright show-trace trace.zip
```