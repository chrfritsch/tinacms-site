---
id: /docs/contributing/setting-up
title: Contribution Set-up
prev: /docs/contributing/guidelines
next: /docs/contributing/troubleshooting
---

## Development

To get started:

```bash
git clone git@github.com:tinacms/tinacms.git
cd tinacms
npm install
npm run bootstrap
npm run build

# Start the Gatsby demo
cd packages/demo-gatsby
npm run start
```

<tip>**TinaCMS** uses [**Lerna**](https://lerna.js.org/) to manage dependencies when developing locally. This allows the various packages to reference each other via symlinks. Running `npm install` from within a package replaces the symlinks with references to the packages in the npm registry.</tip>

## Commands

| Commands                           | Description                                   |
| ---------------------------------- | --------------------------------------------- |
| npm run bootstrap                  | Install dependencies and link local packages. |
| npm run build                      | Build all packages                            |
| npm run test                       | Run tests for all packages                    |
| lerna run build --scope \<package> | Build only \<package>.                        |
| lerna run watch --parallel         | Watch all packages for rebuilds.              |

## Links

- [Circle CI](https://circleci.com/gh/tinacms/tinacms): Continuous Integration
