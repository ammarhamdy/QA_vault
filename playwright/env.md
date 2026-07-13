
```
npm install dotenv @types/dotenv --save-dev
```


How to use `doenv`
```ts
import dotenv from 'dotenv';

dotenv.config();

export default defineConfig({
...
use: {

	/* Base URL to use in actions like `await page.goto('')`. */
	baseURL: process.env.BASE_URL || 'https://aljazeaonline.codlop.sa',
	  
	/* Collect trace when retrying the failed test. See https://playwright.dev/docs/trace-viewer */
	trace: 'on-first-retry',

},
...
```

