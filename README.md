![Logo](admin/meter-statistics.png)
# ioBroker.meter-statistics

[![NPM version](https://img.shields.io/npm/v/iobroker.meter-statistics.svg)](https://www.npmjs.com/package/iobroker.meter-statistics)
[![Downloads](https://img.shields.io/npm/dm/iobroker.meter-statistics.svg)](https://www.npmjs.com/package/iobroker.meter-statistics)
![Number of Installations](https://iobroker.live/badges/meter-statistics-installed.svg)
![Current version in stable repository](https://iobroker.live/badges/meter-statistics-stable.svg)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

[![NPM](https://nodei.co/npm/iobroker.meter-statistics.png?downloads=true)](https://nodei.co/npm/iobroker.meter-statistics/)

**Tests:** ![Test and Release](https://github.com/jb-io/ioBroker.meter-statistics/workflows/Test%20and%20Release/badge.svg)

## meter-statistics adapter for ioBroker

Calculate statistics from any smart meter

## Developer manual
This section is intended for the developer. It can be deleted later

### Getting started

You are almost done, only a few steps left:
1. Create a new repository on GitHub with the name `ioBroker.meter-statistics`
1. Initialize the current folder as a new git repository:  
    ```bash
    git init -b master
    git add .
    git commit -m "Initial commit"
    ```
1. Link your local repository with the one on GitHub:  
    ```bash
    git remote add origin https://github.com/jb-io/ioBroker.meter-statistics
    ```

1. Push all files to the GitHub repo:  
    ```bash
    git push origin master
    ```
1. Add a new secret under https://github.com/jb-io/ioBroker.meter-statistics/settings/secrets. It must be named `AUTO_MERGE_TOKEN` and contain a personal access token with push access to the repository, e.g. yours. You can create a new token under https://github.com/settings/tokens.

1. Head over to [src/main.ts](src/main.ts) and start programming!

### Best Practices
We've collected some [best practices](https://github.com/ioBroker/ioBroker.repositories#development-and-coding-best-practices) regarding ioBroker development and coding in general. If you're new to ioBroker or Node.js, you should
check them out. If you're already experienced, you should also take a look at them - you might learn something new :)

### Scripts in `package.json`
Several npm scripts are predefined for your convenience. You can run them using `npm run <scriptname>`
| Script name | Description |
|-------------|-------------|
| `build` | Compile the TypeScript sources. |
| `watch` | Compile the TypeScript sources and watch for changes. |
| `test:ts` | Executes the tests you defined in `*.test.ts` files. |
| `test:package` | Ensures your `package.json` and `io-package.json` are valid. |
| `test:integration` | Tests the adapter startup with an actual instance of ioBroker. |
| `test` | Performs a minimal test run on package files and your tests. |
| `check` | Performs a type-check on your code (without compiling anything). |
| `lint` | Runs `ESLint` to check your code for formatting errors and potential bugs. |
| `translate` | Translates texts in your adapter to all required languages, see [`@iobroker/adapter-dev`](https://github.com/ioBroker/adapter-dev#manage-translations) for more details. |
| `release` | Creates a new release, see [`@alcalzone/release-script`](https://github.com/AlCalzone/release-script#usage) for more details. |

### Configuring the compilation
The adapter template uses [esbuild](https://esbuild.github.io/) to compile TypeScript and/or React code. You can configure many compilation settings 
either in `tsconfig.json` or by changing options for the build tasks. These options are described in detail in the
[`@iobroker/adapter-dev` documentation](https://github.com/ioBroker/adapter-dev#compile-adapter-files).

### Writing tests
When done right, testing code is invaluable, because it gives you the 
confidence to change your code while knowing exactly if and when 
something breaks. A good read on the topic of test-driven development 
is https://hackernoon.com/introduction-to-test-driven-development-tdd-61a13bc92d92. 
Although writing tests before the code might seem strange at first, but it has very 
clear upsides.

The template provides you with basic tests for the adapter startup and package files.
It is recommended that you add your own tests into the mix.

### Publishing the adapter
Using GitHub Actions, you can enable automatic releases on npm whenever you push a new git tag that matches the form 
`v<major>.<minor>.<patch>`. We **strongly recommend** that you do. The necessary steps are described in `.github/workflows/test-and-release.yml`.

Since you installed the release script, you can create a new
release simply by calling:
```bash
npm run release
```
Additional command line options for the release script are explained in the
[release-script documentation](https://github.com/AlCalzone/release-script#command-line).

To get your adapter released in ioBroker, please refer to the documentation 
of [ioBroker.repositories](https://github.com/ioBroker/ioBroker.repositories#requirements-for-adapter-to-get-added-to-the-latest-repository).

### Test the adapter manually with dev-server
Since you set up `dev-server`, you can use it to run, test and debug your adapter.

You may start `dev-server` by calling from your dev directory:
```bash
dev-server watch
```

The ioBroker.admin interface will then be available at http://localhost:8081/

Please refer to the [`dev-server` documentation](https://github.com/ioBroker/dev-server#command-line) for more details.

## Open Tasks
* [TODO] Insert Translation
* [TODO] Create README
* [TODO] Respect start value date
* [TODO] Automated update of startvalue on year change

## Changelog
<!--
    Placeholder for the next version (at the beginning of the line):
    ### **WORK IN PROGRESS**
-->
### 0.1.1 (2023-03-29)
* [FEATURE] Add device icons

### 0.1.0 (2023-03-18)
* [TASK] Code refactoring
* [TASK] Add test cases

### 0.0.4 (2023-03-05)
* [BUGFIX] Fix calculation of predicted total
* [TASK] Update project

### 0.0.3 (2023-03-04)
* Add predicted consumption

### 0.0.2 (2023-03-04)
* Change Logo

### 0.0.1 (2023-03-01)
* (jb-io) initial release

## License

[Licensed under GPLv3](LICENSE) Copyright (c) 2023 jb-io
