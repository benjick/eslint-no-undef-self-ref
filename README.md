ESLint doesn't warn about `no-undef` when doing an assignment to the same name as the name of the variable, e.g. `var foo = foo;`.

To reproduce clone this repo, run `npm install` followed by `npm test`

Expected output:

```
eslint-no-undef-self-ref/index.js
  1:11  warning  'quz' is not defined  no-undef
  2:11  warning  'foo' is not defined  no-undef

✖ 2 problems (0 errors, 2 warnings)
```

Actual output:
```
eslint-no-undef-self-ref/index.js
  1:11  warning  'quz' is not defined  no-undef

✖ 1 problem (0 errors, 1 warning)
```
