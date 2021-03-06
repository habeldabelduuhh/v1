# Aurelia 1 scaffolding skeleton

![CI](https://github.com/aurelia/v1/workflows/CI/badge.svg) ![E2E-Linux](https://github.com/aurelia/v1/workflows/E2E-Linux/badge.svg) ![E2E-Windows](https://github.com/aurelia/v1/workflows/E2E-Windows/badge.svg) ![E2E-macOS](https://github.com/aurelia/v1/workflows/E2E-macOS/badge.svg)

_Work In Progress_ (Note ready. Converting aurelia-cli inner skeleton to here...)

The scaffolding repo for Aurelia 1 used by the [makes](https://makes.js.org) tool to create new Aurelia 1 projects.

Extracted from original aurelia-cli skeleton folder.

## Create an Aurelia 1 project

First, ensure that you have Node.js v8.9.0 or above installed on your system. Next, using [npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b),
a tool distributed as part of Node.js, we'll create a new Aurelia 1 app. At a command prompt, run the following command:

```bash
npx makes aurelia/v1
```

This will cause `npx` to download the `makes` tool, along with the `aurelia/v1` scaffold from this repo, which it will use
to guide you through creating your project.

## Aurelia CLI

Aurelia CLI v2.0.0+ uses this repo to create new user app. When users run

```bash
au1 new
```

It calls `npx makes aurelia/v1` to perform the scaffolding.

## Test

Unit tests for various "makes" files.

```bash
npm test
```

E2e tests for skeletons. Run 72 skeletons, very slow.

```bash
npm run test:e2e
```

Better to run a subset.
```bash
npx cross-env TARGET_FEATURES=webpack,babel npm run test:e2e
```

To test with an aurelia-cli master/branch/tag/commit.
```bash
npx cross-env TARGET_FEATURES=webpack,babel TARGET_CLI=aurelia/cli#branch npm run test:e2e
```

## License

MIT.
