# get-jwks-ts-issue
Demonstration of a TS compilation issue with the get-jwks package

### Setup

To install dependencies and set up pnpm, run the following:
```sh
npm run setdev
```

### Reproduce problem

If you try to compile the project with:
```sh
pnpm build
```

You will get the following error:
```
•100% ➜ pnpm build

> get-jwks-ts-issue@1.0.0 build .../get-jwks-ts-issue
> tsc -p tsconfig.json

src/index.ts:2:1 - error TS2349: This expression is not callable.
  Type 'typeof import(".../get-jwks-ts-issue/node_modules/.pnpm/get-jwks@8.3.1/node_modules/get-jwks/src/get-jwks")' has no call signatures.

2 buildGetJwks()
  ~~~~~~~~~~~~


Found 1 error in src/index.ts:2

 ELIFECYCLE  Command failed with exit code 2.
```
