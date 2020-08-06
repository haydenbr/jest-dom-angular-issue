# Jest Dom Angular Issue

When attempting to import `jest-dom` (via `import '@testing-library/jest-dom'` in `setup-jest.ts`) I get the following error when trying to run jest:

```
FAIL  src/app/app.component.spec.ts
● Test suite failed to run

	TypeError: Cannot set property 'escape' of null

		1 | import 'jest-preset-angular';
		2 | import './jest-global-mocks';
	> 3 | import '@testing-library/jest-dom'
			| ^
		4 |

		at node_modules/css.escape/css.escape.js:103:18
		at Object.<anonymous> (src/setup-jest.ts:3:1)
```

I've copied the contents of the npm debug report to this repo at `./debug.log`.

System information:

node: v12.18.3
npm: 6.14.6

I setup jest according to [jest-preset-angular](https://github.com/thymikee/jest-preset-angular)

Steps to reproduce:

```
npm install
npm run test
```
